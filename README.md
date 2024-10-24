# Delphi-GEmail
Delphi class to send an email using gmail.
Класс Delphi для отправки электронной почты через Gmail

 Use sample:

````Delphi
  Gmail := TcfsGmail.Create('YourAccount@gmail.com', 'App password', 'From you/company', 'YourAccount@gmail.com', Host, Port);
  try
    try
      Gmail.Connect;
      Gmail.Send(['useremail@gmail.com'], 'Subject', 'PlainBody', 'htmlBody', 'AttachmentFile');
    except
      on E: Exception do
        ShowMessage(E.Message);
    end;
  finally
    GEmail.Free;
  end;
  
````

NOTE 1: Add in your executable file path the two openSSL Libraries:  "libeay32.dll"  and  "ssleay32.dll".

NOTE 2: Configure your email "YourAccount@gmail.com" account to allow sending mails from and external app:  Enter in your Personnal Setting (gmail) go to "Security": Activate “2-Step Verification” and add “App Password” or Activate "Allow less secure apps "
