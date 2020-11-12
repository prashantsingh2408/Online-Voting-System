# Online voting system

## Admin Features
* Login
* Manage Parties
* Manage Users
* Check Poll Results
* Update Password
* Update Profile
* Block & unblock users
* Restart Voting
* Announce the result.
* Start and stop voting using timer (Read rule no 7)
* Logout
## Voter/User Features
* Registration
* Login
* Update Profile
* Email verification using OTP or token
* Give Vote
* Forget password

## Instructions
1. Import webbixun.sql into database
2. Run Index.php 
3. Install
   ``` composer require phpmailer/phpmailer```
   * for senting OTP
4. Home Page
  * ```index.html``` (home Page)
5. OTP and password
  * ```forgetPassGetOTP.php ``` (retrive password by mail sending OTP)
  *  ``` updatePwd.php ``` (update password for admin, user and at time of password resent) 
6. Login
   ```user.html```
   * For login user
7. For user reseting  password by OTP
  * ```forgetPass.php```
8. For getting OTP
 * ```forgetPassGetOTP.php```
 * configuration on phpmailer
 ``` 
 //Server settings
            $mail->SMTPDebug = SMTP::DEBUG_SERVER;                      // Enable verbose debug output
            $mail->isSMTP();                                            // Send using SMTP
            $mail->Host       = 'smtp.gmail.com';                    // Set the SMTP server to send through
            $mail->SMTPAuth   = true;                                   // Enable SMTP authentication
            $mail->Username   = 'mailerphpemail@gmail.com';                     // SMTP username
            $mail->Password   = 'maileremailpass';                               // SMTP password
            //$mail->SMTPSecure = PHPMailer::ENCRYPTION_STARTTLS;         // Enable TLS encryption; `PHPMailer::ENCRYPTION_SMTPS` encouraged
            $mail->Port       = 587;                                    // TCP port to connect to, use 465 for `PHPMailer::ENCRYPTION_SMTPS` above

            //Recipients
            $mail->setFrom('from@example.com', 'Mailer');
            $mail->addAddress('prashantsingh2408@gmail.com', 'prashant singh');     // Add a recipient
            $mail->addAddress('ellen@example.com');               // Name is optional
            $mail->addReplyTo('info@example.com', 'Information');
            $mail->addCC('cc@example.com');
            $mail->addBCC('bcc@example.com');

            // Attachments
            //$mail->addAttachment('/var/tmp/file.tar.gz');         // Add attachments
            //$mail->addAttachment('/tmp/image.jpg', 'new.jpg');    // Optional name

            // Content
            $mail->isHTML(true);                                  // Set email format to HTML
            $mail->Subject = 'You OTP from Webixiun limited  ';
            $mail->Body  = $OTP;
            $mail->AltBody = 'This is the body in plain text for non-HTML mail clients';
 ```
  9. set new password 
    * ``` newPassUser.php```
 10. Update password if OTP correct
      * updatePwd.php
  
    
    

   
