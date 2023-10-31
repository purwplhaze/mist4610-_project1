# mist4610_project1

# Creation of Database

SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0;
SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0;
SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION';

-- -----------------------------------------------------
-- Schema cs_g9p1
-- -----------------------------------------------------

-- -----------------------------------------------------
-- Schema cs_g9p1
-- -----------------------------------------------------
CREATE SCHEMA IF NOT EXISTS `cs_g9p1` DEFAULT CHARACTER SET utf8 ;
USE `cs_g9p1` ;

-- -----------------------------------------------------
-- Table `cs_g9p1`.`coach`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`coach` (
  `coachid` INT NOT NULL,
  `coach_f_name` VARCHAR(45) NULL,
  `coach_l_name` VARCHAR(45) NULL,
  `coach_experience` VARCHAR(45) NULL,
  `coach_contact_info` VARCHAR(45) NULL,
  PRIMARY KEY (`coachid`))
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`team`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`team` (
  `teamid` INT NOT NULL,
  `team_name` VARCHAR(45) NULL,
  `team_age_range` VARCHAR(45) NULL,
  `team_mascot` VARCHAR(45) NULL,
  `coach_coachid` INT NOT NULL,
  `team_teamid` INT NOT NULL,
  PRIMARY KEY (`teamid`),
  INDEX `fk_team_coach1_idx` (`coach_coachid` ASC) VISIBLE,
  INDEX `fk_team_team1_idx` (`team_teamid` ASC) VISIBLE,
  CONSTRAINT `fk_team_coach1`
    FOREIGN KEY (`coach_coachid`)
    REFERENCES `cs_g9p1`.`coach` (`coachid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION,
  CONSTRAINT `fk_team_team1`
    FOREIGN KEY (`team_teamid`)
    REFERENCES `cs_g9p1`.`team` (`teamid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`player`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`player` (
  `playerid` INT NOT NULL,
  `player_f_name` VARCHAR(45) NULL,
  `player_l_name` VARCHAR(45) NULL,
  `player_dob` VARCHAR(45) NULL,
  `player_contact_info` VARCHAR(45) NULL,
  `player_member_status` VARCHAR(45) NULL,
  `team_teamid` INT NOT NULL,
  PRIMARY KEY (`playerid`),
  INDEX `fk_player_team1_idx` (`team_teamid` ASC) VISIBLE,
  CONSTRAINT `fk_player_team1`
    FOREIGN KEY (`team_teamid`)
    REFERENCES `cs_g9p1`.`team` (`teamid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`facility`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`facility` (
  `facilityid` INT NOT NULL,
  `facility_name` VARCHAR(45) NULL,
  `facility_type` VARCHAR(45) NULL,
  `facility_availability` DATETIME NULL,
  PRIMARY KEY (`facilityid`))
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`rental of facility`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`rental of facility` (
  `fac_rentid` INT NOT NULL,
  `book_time` DATETIME NULL,
  `book_date` DATE NULL,
  `renter_name` VARCHAR(45) NULL,
  `renter_contact_info` VARCHAR(45) NULL,
  `facility_facilityid` INT NOT NULL,
  `team_teamid` INT NOT NULL,
  PRIMARY KEY (`fac_rentid`),
  INDEX `fk_facility registration_facility1_idx` (`facility_facilityid` ASC) VISIBLE,
  INDEX `fk_rental of facility_team1_idx` (`team_teamid` ASC) VISIBLE,
  CONSTRAINT `fk_facility registration_facility1`
    FOREIGN KEY (`facility_facilityid`)
    REFERENCES `cs_g9p1`.`facility` (`facilityid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION,
  CONSTRAINT `fk_rental of facility_team1`
    FOREIGN KEY (`team_teamid`)
    REFERENCES `cs_g9p1`.`team` (`teamid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`event`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`event` (
  `event_id` INT NOT NULL,
  `event_name` VARCHAR(45) NULL,
  `event_date` VARCHAR(45) NULL,
  `event_type` VARCHAR(45) NULL,
  `event_result` VARCHAR(45) NULL,
  `event_time` VARCHAR(45) NULL,
  `rental of facility_fac_rentid` INT NOT NULL,
  PRIMARY KEY (`event_id`),
  INDEX `fk_event_rental of facility1_idx` (`rental of facility_fac_rentid` ASC) VISIBLE,
  CONSTRAINT `fk_event_rental of facility1`
    FOREIGN KEY (`rental of facility_fac_rentid`)
    REFERENCES `cs_g9p1`.`rental of facility` (`fac_rentid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`staff`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`staff` (
  `staffid` INT NOT NULL,
  `staff_name` VARCHAR(45) NULL,
  `staff_contact_info` VARCHAR(45) NULL,
  `staff_position` VARCHAR(45) NULL,
  `team_teamid` INT NOT NULL,
  PRIMARY KEY (`staffid`),
  INDEX `fk_staff_team1_idx` (`team_teamid` ASC) VISIBLE,
  CONSTRAINT `fk_staff_team1`
    FOREIGN KEY (`team_teamid`)
    REFERENCES `cs_g9p1`.`team` (`teamid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`sponser`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`sponser` (
  `sponserid` INT NOT NULL,
  `sponser_f_name` VARCHAR(45) NULL,
  `sponser_l_name` VARCHAR(45) NULL,
  `sponser_contact_info` VARCHAR(45) NULL,
  PRIMARY KEY (`sponserid`))
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`donation`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`donation` (
  `donationid` INT NOT NULL,
  `donor_f_name` VARCHAR(45) NULL,
  `donor_l_name` VARCHAR(45) NULL,
  `donation_amount` INT NULL,
  `donation_date` DATE NULL,
  `sponser_sponserid` INT NOT NULL,
  `team_teamid` INT NOT NULL,
  PRIMARY KEY (`donationid`),
  INDEX `fk_donation_sponser1_idx` (`sponser_sponserid` ASC) VISIBLE,
  INDEX `fk_donation_team1_idx` (`team_teamid` ASC) VISIBLE,
  CONSTRAINT `fk_donation_sponser1`
    FOREIGN KEY (`sponser_sponserid`)
    REFERENCES `cs_g9p1`.`sponser` (`sponserid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION,
  CONSTRAINT `fk_donation_team1`
    FOREIGN KEY (`team_teamid`)
    REFERENCES `cs_g9p1`.`team` (`teamid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`injury`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`injury` (
  `injuryid` INT NOT NULL,
  `injury_date` VARCHAR(45) NULL,
  `injury_body_part` VARCHAR(45) NULL,
  `injury_severity` VARCHAR(45) NULL,
  `player_playerid` INT NOT NULL,
  PRIMARY KEY (`injuryid`),
  INDEX `fk_injury_player1_idx` (`player_playerid` ASC) VISIBLE,
  CONSTRAINT `fk_injury_player1`
    FOREIGN KEY (`player_playerid`)
    REFERENCES `cs_g9p1`.`player` (`playerid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`equipment`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`equipment` (
  `equipmentid` INT NOT NULL,
  `equipment_name` VARCHAR(45) NULL,
  `equipment_quantity` VARCHAR(45) NULL,
  `equipment_condition` VARCHAR(45) NULL,
  `equipment checkout_equip_checkid` INT NOT NULL,
  PRIMARY KEY (`equipmentid`))
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`event registration`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`event registration` (
  `event_event_id` INT NOT NULL,
  `team_teamid` INT NOT NULL,
  PRIMARY KEY (`event_event_id`, `team_teamid`),
  INDEX `fk_event_has_team_team1_idx` (`team_teamid` ASC) VISIBLE,
  INDEX `fk_event_has_team_event_idx` (`event_event_id` ASC) VISIBLE,
  CONSTRAINT `fk_event_has_team_event`
    FOREIGN KEY (`event_event_id`)
    REFERENCES `cs_g9p1`.`event` (`event_id`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION,
  CONSTRAINT `fk_event_has_team_team1`
    FOREIGN KEY (`team_teamid`)
    REFERENCES `cs_g9p1`.`team` (`teamid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `cs_g9p1`.`equipment checkout`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `cs_g9p1`.`equipment checkout` (
  `equipment_equipmentid` INT NOT NULL,
  `player_playerid` INT NOT NULL,
  `checkoutid` VARCHAR(45) NOT NULL,
  `checkout_date` DATE NULL,
  `return_date` DATE NULL,
  INDEX `fk_equipment_has_player_player1_idx` (`player_playerid` ASC) VISIBLE,
  INDEX `fk_equipment_has_player_equipment1_idx` (`equipment_equipmentid` ASC) VISIBLE,
  PRIMARY KEY (`checkoutid`),
  CONSTRAINT `fk_equipment_has_player_equipment1`
    FOREIGN KEY (`equipment_equipmentid`)
    REFERENCES `cs_g9p1`.`equipment` (`equipmentid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION,
  CONSTRAINT `fk_equipment_has_player_player1`
    FOREIGN KEY (`player_playerid`)
    REFERENCES `cs_g9p1`.`player` (`playerid`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


SET SQL_MODE=@OLD_SQL_MODE;
SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS;
SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS;
