# Home Automation using Amazon AWS IoT Core & ESP32

## Home Automation Project using Amazon AWS IoT Core & ESP32 WiFi Module.

### The AWS IoT Core is a managed cloud service that lets connected devices easily and securely interact with cloud applications and other devices. The AWS IoT Core MQTT messaging service lets you send and receive MQTT messages to and from AWS IoT Core. Using the Publish/Subscribe feature we can basically receive or send any data to & the AWS IoT Core dashboard.


### Circuit Diagram & Hardware Design
Let us take a look at the Schematic of AWS IoT Core Based Home Automation Project with ESP32. The schematic is drawn using the Altium Designer Software.


![img25](https://github.com/user-attachments/assets/6d89c1e8-80be-44eb-85f7-5befc84483c9)

### Setting up Amazon AWS IoT Core Dashboard

The signing up part for the Amazon Web Services is already explained in the previous post. You can follow the AWS IoT Core Getting Started tutorial.

After successfully signing in, the AWS Management Console window will open. In the services search tab at the top right ‘IoT core’ & hit enter.

![img13](https://github.com/user-attachments/assets/dc332c2c-a0c5-4fa0-9509-c181ec4b3edb)

You can click on IoT Core, so an AWS IoT Dashboard will appear now.

![img14](https://github.com/user-attachments/assets/5b5001a7-df30-4f25-9775-4c4f0dd7941d)

* On the left side of the dashboard, there are so many options. But we need to work with two options here. One is the manage option and the other one is the secure option.


* Creating a Thing
Now we need to create a thing associated with our project. For this, follow the following steps:

Specifying thing properties
Configuring device certificate
Attaching policies to certificate
Under the manage option click on Thing. Now we need to create a Thing here. So, click on Create Things here.

![img15](https://github.com/user-attachments/assets/d2cf6f1b-f75c-4d86-83f1-be645a93438d)


You can select whether create a single thing or create many things. But for our applications, select create a single thing. Then click on Next.

![img16](https://github.com/user-attachments/assets/f58a3fe2-fe81-44c4-bf2c-2f087d965f7f)

* Specify Thing Properties
Here we need to specify the Thing properties. First, give a thing name. You can name it anything. For example, I will name it Home_Automation.

![img17](https://github.com/user-attachments/assets/edfce5a7-5585-46f0-8e2c-2195a77e3b4c)

Under additional configurations, there is no need to make any changes.

Under the device shadow option, select the first option as No shadow. Then click on Next.


![img18](https://github.com/user-attachments/assets/2939e14d-b175-4de2-b219-37266de93ac3)


* Generate Device Certificate
Now you need to configure device certificate. So here you can auto-generate a new certificate or use your own certificate or upload CSR or skip this.

![img19](https://github.com/user-attachments/assets/3d4bb8d9-f773-4421-81ed-74e460213073)


But the AWS recommendation is to select the Auto Generate New Certificate. Then click on Next.

Create & Attach Policy
Now we need to attach a policy to the Things we created. But no policies are here right now. So we need to create a policy first.


![img20](https://github.com/user-attachments/assets/f9efe2f1-196e-4f9d-b093-c7b047954217)


So click on create policy. Here give any name to the policy. For example, I will give it a name as “Automation_Policy“.


Now the add statement part is very important. Under the action, type IoT. So multiple options will pop up. From here we will only need to Subscribe, Connect and Receive.

![img21](https://github.com/user-attachments/assets/167e2de0-ab26-4190-b64f-fb2cd35c4473)

Now click on create to create the policy. So the policy has been created successfully.

Now go back to Create Thing option. So a policy option will appear. We need to attach the policies to the certificate. So select the appeared policy and click on create a thing.

![img22](https://github.com/user-attachments/assets/6bb33675-a45c-41ed-87e7-11bdba934d7d)


* Downloading Certificates and Keys
Now we need to download the required certificates from this list.


<img width="612" height="938" alt="img23" src="https://github.com/user-attachments/assets/1e4a4909-3c44-4db6-91da-d65c652a7d99" />


First, download the device certificate and then rename it as a device certificate for identification.

Also, download the public key and rename it as a public key. Then download the private key and rename it as a private key.

In the Root CA Certificates, there are two certificates here. But we just need a Root CA1 certificate, so download it as well.

![img23](https://github.com/user-attachments/assets/50099c91-6461-471f-8d70-6145ed093bba)

So we have downloaded all the certificates that we need for our project.



