# 01 Challange File


## 1.1 Evidence that proof mail is fake or real
> Given - Mail Sample Image and Mail Header

**Analysis -**
1. Visual Analysis - Mail from in.airtel.com, Seems Phishy, As Actual Airtel website is airtel.in not airtel.com
2. On Check Headers -
    1. In message id it says ```<CALn1_W-vBUf+sfqw1BHT8hYu1pzdB3VS6bcPLGGTgT8KonWwJw@91.235.116.230>``` Clearly not originating from actual airtel domain. 
    2. On further diving into the email body,
       ```
       <div dir=3D"ltr"><div dir=3D"ltr"><div>Hi Steve,</div><div><br></div><div>T=
        his is with regard to the services that we provide to your company. It is t=
        he end of the year and we would like your confirmation of the services.</di=
        v><div><br></div><div>To continue to receive our services, pls provide your=
        confirmation.=C2=A0</div><div><a href=3D"http://91.235.116.230/customer/pa=
        nel_login.php?id=3D9109812001%user%service%confirmation%%yes=3Dno"> https:/=
        /www.airtel.in/customer/panel_login.php?id=3D9109812001%user%service%confir=
        mation%%yes=3Dno</a><br></div><div><br></div><div>PFA the detailed list of =
        services and the total bill.<br></div><div><br></div><div><br></div><div>Th=
        anks,</div><div>John Adams,</div><div>Customer Sales Representative, Airtel=
        <br></div></div></div>
       ```
       In here we can see, there is a <herf> tag being using direcirectng to ```http://91.235.116.230/customer/pa=
        nel_login.php?id=3D9109812001%user%service%confirmation%%yes=3Dno``` Which indicates a clear phising link.
3. We can conclude this is a fake email.

## 1.2 Find the location from where the mail came.

I tried whosis on the ip and got the result as
```
address:        ROMANIA
address:        Iancu Jianu
address:        237220
address:        Barbu Stirbei FN, imobil C1
```

## 1.3 Mail server name with evidence etc.

In the header in the recieved from ```EHLO mail-il1-f172.91.235.116.230```, 
The this ip is owned by ```thcservers.com```

## 1.4 Find out its a spoof mail or it's sent by hacked account.

This i a spoof mail, As the sender is using servers from Romaina. Also the domain ```in.airtel.com``` is not owned by airtel.
Is it was a hacked account, the domain would have been airtel.in. Also in the message id it shows ```<CALn1_W-vBUf+sfqw1BHT8hYu1pzdB3VS6bcPLGGTgT8KonWwJw@91.235.116.230>```, Which clearly defines it is a spoof email.

## 3 Find out its a real page of fake

This is a 3D phising attack, as the link contains a base64 encoded string in the url 
```PGlmcmFtZSBzcmM94oCdaHR0cHM6Ly9zZWN1cml0eS1zZXJ2aWNlLm5lZWwuc3lzdGVtLmNvbeKAnSBoZWlnaHQ94oCdMTAwJeKAsyB3aWR0aD3igJ0xMDAl4oCzPjwvaWZyYW1lPg==``` which decodes to <br>
```<iframe src=”https://security-service.neel.system.com” height=”100%″ width=”100%″></iframe>```<br>

## 4 Which one is correct from the options below?

The given 2 strings looks similar, as these are a part of Homoglyph attack, i used reversing, generated new homoglyph for both the strings on irongeek, which takes input in english. When i tried to generate for the first one, i was able to generate for all characters, but for the string `b` i was unable to generate for P and C which indicates a homoglyph.
