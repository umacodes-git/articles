**Setting up Charles Proxy in macOS**

1. Download and install charles proxy from - https://www.charlesproxy.com/.<br></br>
2. Open the app.<br></br>
3. Go to: `Help > SSL Proxying > Install Charles Root Certificate`<br></br>
4. Add the root certificate to login key chain.<br></br>
!["Install root certificate"](install_root_cert.png)<br></br>
!["Add root certificate to keychain"](01_add_cert_keychain.png)<br></br>


**Inspecting iOS Simulator Traffice**
1. Install the Root Certificate in iOS Simulator in use for testing.
(To install iOS Siumulators - Download Xcode from App Store)<br></br>
!["Install iOS Simulator Certificate"](install_rcert_simulator.png)<br></br>
2. Trust the installed certificate in Simulator. <br></br>
!["Trust Charles certificate"](trust_charles_certificate.png)
3. Run the app from `Xcode`. (Checkout the source code from your team's repository or get it from development team.)<br></br>

**Note:**
When inspecting network requests via `Charles` always launch Charles first and launch the mobile app next. If the app is launched first Charles app will not record any requests.

4. Push the start recording button in Charles app.<br></br>
!["Stop Recording"](charles_rec_off.png)
!["Start Recording"](charles_rec_on.png)<br></br>

5. Now you can see all the network requests from the mobile device or simulator connected. I have just filtered on a specific request - `https://api.stackexchange.com/2.2/users?order=desc&sort=reputation&site=stackoverflow` for example.<br></br>
!["Charles sample response page"](charles_sample_response.png)<br></br>

**Inspecting network traffic in an Andrid Device**
1. Go to `Help > SSL Proxying > Install Charles Root Certificate on a Mobile Device or Remote Browser `.<br></br>
!["Config Charles for Mobile Device"](install_cert_remote_device.png)<br></br>
2. Follow the instructions from Charles.
!["Remote device Charles instruction"](remote_device_proxy_setup_message.png)
3. Configure your test Android device with proxy address from Charles app and save proxy settings.<br></br>
!["Android device proxy setup"](android_device_proxy.png)<br></br>
4. Visit `chls.pro/ssl` from the device.<br></br>
!["Charles certificate downloaded"](cert_downloaded.png)<br></br>
5. Open the downloaded certificate to trust it and save.<br></br>
!["Trust certificate"](install_charles_rcert.png)

Now you can see all the traffic from test mobile device.