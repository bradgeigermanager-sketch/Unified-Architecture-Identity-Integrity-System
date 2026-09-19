CREATE TABLE Identity (
    identityId VARCHAR(64) PRIMARY KEY,
    identityType VARCHAR(64),
    attributes JSON,
    continuityMarkers JSON
);

CREATE TABLE Record (
    recordId VARCHAR(64) PRIMARY KEY,
    identityId VARCHAR(64),
    domain VARCHAR(64),
    recordType VARCHAR(64),
    attributes JSON,
    timestamp DATETIME,
    confidenceScore FLOAT,
    FOREIGN KEY (identityId) REFERENCES Identity(identityId)
);

CREATE TABLE Provenance (
    recordId VARCHAR(64),
    source VARCHAR(128),
    timestamp DATETIME,
    method VARCHAR(128),
    confidence FLOAT,
    PRIMARY KEY (recordId),
    FOREIGN KEY (recordId) REFERENCES Record(recordId)
);

CREATE TABLE Anomaly (
    anomalyId VARCHAR(64) PRIMARY KEY,
    identityId VARCHAR(64),
    anomalyType VARCHAR(64),
    severity INT,
    attributes JSON,
    relatedRecords JSON,
    relatedDomains JSON,
    FOREIGN KEY (identityId) REFERENCES Identity(identityId)
);

CREATE TABLE Task (
    taskId VARCHAR(64) PRIMARY KEY,
    description TEXT,
    domain VARCHAR(64),
    inputs JSON,
    outputs JSON,
    validation TEXT,
    dependencies JSON
);

CREATE TABLE Procedure (
    procedureId VARCHAR(64) PRIMARY KEY,
    steps JSON,
    preconditions JSON,
    postconditions JSON,
    errorHandling JSON,
    requiredTools JSON
);

CREATE TABLE Tool (
    toolId VARCHAR(64) PRIMARY KEY,
    purpose TEXT,
    inputs JSON,
    outputs JSON,
    integrationPoints JSON,
    domain VARCHAR(64)
);

CREATE TABLE Goal (
    goalId VARCHAR(64) PRIMARY KEY,
    description TEXT,
    goalType VARCHAR(64),
    tasks JSON,
    subGoals JSON,
    priority INT
);
