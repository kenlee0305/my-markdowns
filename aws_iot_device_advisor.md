# AWS IoT Device Advisor setup and test configurations

## Note from AWS
    Device Advisor is supported in us-east-1, us-west-2, ap-northeast-1, and eu-west-1 regions.

## Setup for Device Advisor
1. Create an IoT thing
2. Create an IAM role to be used as your device role
3. Create a custom-managed policy for an IAM user to use Device Advisor
4. Create an IAM user to use Device Advisor
5. Configure your device

## Device Advisor workflow
1. Prerequisites
2. Create a test suite definition
3. Get a test suite definition
4. Get a test endpoint
5. Start a test suite run
6. Get a test suite run
7. Stop a test suite run
8. Get a qualification report for a successful qualification test suite run
   
## Pre-built tests in Device Advisor
### Premissions and policies
- [X] "Device certificate attached policies don’t contain wildcards"
  
### MQTT
1. CONNECT, DISCONNECT, and RECONNECT  

   - [X] "Device send CONNECT to AWS IoT Core (Happy case)"
   - [ ] "Device can return PUBACK to an arbitrary topic for QoS1"

   - [ ] "Device connect retries with jitter backoff - No CONNACK response"
   - [ ] "Device connect retries with exponential backoff - No CONNACK response"
   - [ ] "Device re-connect with jitter backoff - After server disconnect"
  
2. Keep-Alive
   
   - [X] "Mqtt No Ack PingResp"  

3. Publish
   - [X] "QoS0 (Happy Case)"
   - [X] "QoS1 publish retry - No PUBACK"  
  
4. Subscribe
   - [X] "Can Subscribe (Happy Case)"
   - [X] "Subscribe Retry - No SUBACK"

5. Persistent Session
   - [ ] "Persistent Session (Happy Case)"

### Job execution
- [ ] "Device can complete a job execution"

## References
1. https://docs.aws.amazon.com/iot/latest/developerguide/device-advisor.html
2. https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/iotdeviceadvisor.html
3. https://docs.aws.amazon.com/iot/latest/apireference/API_iotdeviceadvisor_CreateSuiteDefinition.html
   