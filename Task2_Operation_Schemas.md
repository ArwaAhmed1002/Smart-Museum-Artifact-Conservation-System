# Smart Museum Artifact Conservation System

## Task 2: Complete Operation Schemas

## Operation 1: Perform Sensor Self-Check

### Purpose
To verify that all essential sensors are working correctly.

### Preconditions
- Chamber is powered on.
- Essential sensors are connected.

### Inputs
- Temperature sensor
- Humidity sensor
- Light sensor
- Vibration sensor
- Door sensor

### Processing
1. Test each essential sensor.
2. Check sensor responses.
3. Identify faulty sensors.
4. Generate the self-check result.

### Outputs
- Sensor self-check result

### Postconditions
- All essential sensors are confirmed to be working.
- System can proceed to normal monitoring.

### Exceptions
- One or more essential sensors fail.


## Operation 2: Register Artifact

### Purpose
To record the identification information of the artifact.

### Preconditions
- Artifact is placed inside the chamber.

### Inputs
- Artifact ID
- Artifact identification information

### Processing
1. Receive artifact information.
2. Validate the information.
3. Store the artifact record.

### Outputs
- Artifact record

### Postconditions
- Artifact is successfully registered.

### Exceptions
- Invalid or missing artifact information.


## Operation 3: Load Environmental Profile

### Purpose
To load the environmental requirements specified for the artifact.

### Preconditions
- Artifact is registered.

### Inputs
- Required temperature range
- Required humidity range
- Permitted vibration level
- Other environmental limits

### Processing
1. Retrieve artifact requirements.
2. Validate the environmental limits.
3. Store the environmental profile.

### Outputs
- Loaded environmental profile

### Postconditions
- Required environmental limits are available for monitoring.

### Exceptions
- Environmental profile is missing or invalid.


## Operation 4: Monitor Environmental Conditions

### Purpose
To continuously monitor the chamber environment.

### Preconditions
- Sensors are working.
- Artifact is inside the chamber.

### Inputs
- Temperature
- Humidity
- Light exposure
- Vibration
- Door status

### Processing
1. Read sensor values.
2. Record current environmental conditions.
3. Compare readings with required limits.
4. Detect abnormal conditions.

### Outputs
- Current environmental status

### Postconditions
- Environmental conditions are continuously monitored.

### Exceptions
- Sensor reading is unavailable or invalid.


## Operation 5: Check Chamber Door Status

### Purpose
To determine whether the chamber door is open or closed.

### Preconditions
- Door sensor is working.

### Inputs
- Door sensor reading

### Processing
1. Read the door sensor.
2. Determine the current door status.
3. Report whether the door is open or closed.

### Outputs
- Door status

### Postconditions
- System knows the current chamber door condition.

### Exceptions
- Door sensor failure.


## Operation 6: Compare Temperature with Required Limits

### Purpose
To determine whether the current temperature is within the permitted range.

### Preconditions
- Environmental profile is loaded.
- Temperature sensor is working.

### Inputs
- Current temperature
- Minimum temperature
- Maximum temperature

### Processing
1. Read the current temperature.
2. Compare it with the minimum limit.
3. Compare it with the maximum limit.
4. Determine whether temperature is normal or abnormal.

### Outputs
- Temperature status

### Postconditions
- System determines whether temperature correction is required.

### Exceptions
- Temperature sensor failure.


## Operation 7: Compare Humidity with Required Limits

### Purpose
To determine whether the current humidity is within the permitted range.

### Preconditions
- Environmental profile is loaded.
- Humidity sensor is working.

### Inputs
- Current humidity
- Minimum humidity
- Maximum humidity

### Processing
1. Read the current humidity.
2. Compare it with the minimum limit.
3. Compare it with the maximum limit.
4. Determine whether humidity is normal or abnormal.

### Outputs
- Humidity status

### Postconditions
- System determines whether humidity correction is required.

### Exceptions
- Humidity sensor failure.


## Operation 8: Issue Temperature Correction Command

### Purpose
To correct the temperature when it moves outside the permitted range.

### Preconditions
- Temperature is outside the required range.
- Temperature-control device is available.

### Inputs
- Current temperature
- Required temperature range

### Processing
1. Determine the required temperature correction.
2. Activate the appropriate control mechanism.
3. Apply the correction command.

### Outputs
- Temperature correction command

### Postconditions
- Temperature correction has been attempted.
- System starts verifying the temperature.

### Exceptions
- Temperature-control device is unavailable.


## Operation 9: Issue Humidity Correction Command

### Purpose
To correct the humidity when it moves outside the permitted range.

### Preconditions
- Humidity is outside the required range.
- Humidity-control device is available.

### Inputs
- Current humidity
- Required humidity range

### Processing
1. Determine the required humidity correction.
2. Activate the appropriate control mechanism.
3. Apply the correction command.

### Outputs
- Humidity correction command

### Postconditions
- Humidity correction has been attempted.
- System starts verifying humidity recovery.

### Exceptions
- Humidity-control device is unavailable.


## Operation 10: Verify Temperature Recovery

### Purpose
To verify that the temperature has returned to the permitted range.

### Preconditions
- Temperature correction command has been issued.

### Inputs
- Current temperature
- Required temperature range
- Allowed recovery period

### Processing
1. Read the temperature sensor.
2. Compare the reading with the required range.
3. Continue monitoring during the recovery period.
4. Determine whether the temperature has recovered.

### Outputs
- Recovery successful or recovery failed

### Postconditions
- Successful recovery allows normal conservation to continue.
- Failed recovery may require a protection response.

### Exceptions
- Temperature does not recover within the allowed period.


## Operation 11: Verify Humidity Recovery

### Purpose
To verify that the humidity has returned to the permitted range.

### Preconditions
- Humidity correction command has been issued.

### Inputs
- Current humidity
- Required humidity range
- Allowed recovery period

### Processing
1. Read the humidity sensor.
2. Compare the reading with the required range.
3. Continue monitoring during the recovery period.
4. Determine whether the humidity has recovered.

### Outputs
- Recovery successful or recovery failed

### Postconditions
- Successful recovery allows normal conservation to continue.
- Failed recovery may require a protection response.

### Exceptions
- Humidity does not recover within the allowed period.


## Operation 12: Detect Significant Vibration

### Purpose
To detect vibration that may put the artifact at risk.

### Preconditions
- Artifact is inside the chamber.
- Vibration sensor is working.

### Inputs
- Current vibration level
- Permitted vibration threshold

### Processing
1. Read the vibration sensor.
2. Compare the vibration level with the permitted threshold.
3. Determine whether significant vibration is present.

### Outputs
- Vibration detected or no significant vibration

### Postconditions
- If significant vibration is detected, activities that may increase risk to the artifact can be suspended.

### Exceptions
- Vibration sensor failure.
