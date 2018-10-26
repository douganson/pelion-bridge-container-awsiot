arm PELION Device Shadow bridge for Amazon AWS IoT 
 
10/26/2018: updated bridge - device shadow deletion message cleanups, misc configuration tweaks

10/20/2018: updated bridge - misc cleanups

10/16/2018: updated bridge and properties editor

10/10/2018: updated bridge and properties editor - numerous http retry fixes and enhancements

10/10/2018: updated bridge - IoTHub token expiration fix

10/09/2018: updated bridge - MQTT fixes, HTTP fixes, device discvoery fixes and tweaks, IoTHub fixes, Max # shadows

10/07/2018: updated bridge - lots of fixes for device deletion

10/06/2018: updated bridge - lots of debugging cleanups, iothub fixes

10/05/2018: updated bridge - pagination support added for Pelion and initial scaling tests and fixes

10/03/2018: updated bridge and properties editor - general sync

10/02/2018: updated bridge - fixed shadow count accounting

10/01/2018: updated bridge - updated specific health stat updates

Container Bridge Instance Installation:

1). Clone this repo into a Linux instance that supports docker images

2). cd into the cloned repo and run: ./run-reload-bridge.sh

Once the container instance is live, you must configure the bridge and bind it between your mbed Pelion account and your IoT Account in AWS

1). Create your IAM Access Key ID and Secret Access Key to enable the AWS CLI in your container. Record those values
    You will also need to record the region of your service (i.e. us-east-1, us-west-2, etc...). Please record that as well. 
    For more information on creating the KeyID and Access Key see: https://aws.amazon.com/cli/

2). Next go to https://os.mbed.com and create your mbed Account. You can then request a Pelion developer account using the same credentials at https://portal.us-east-1.mbedcloud.com

3). Once your Pelion account is created, you need to "Access Keys" to create a Pelion API Key/Token. Record the Token Value

Now that you have your:

    - AWS Region (i.e. us-east-1)
    
    - AWS Access Key ID for the AWS IoT CLI

    - AWS Secret Access Key for the AWS IoT CLI

    - Pelion API Key/Token generated

Go to:  https://[[your containers public IP address]]:8234

    - username: "admin" (no quotes)

    - password: "admin" (no quotes)

Enter each of Key ID, Access Key, and Pelion API Token

    - Please press "SAVE" after *each* is entered... 

    - After all 4 are entered and saved, press "RESTART"

Your Pelion bridge should now be configured and operational. 

Bridge source (Apache 2.0 licensed - Enjoy!): https://github.com/ARMmbed/pelion-bridge.git

Copyright 2018. ARM Ltd. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License. 
