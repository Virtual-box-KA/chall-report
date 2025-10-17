# 01 Challange File


## 1. Evidence that proof mail is fake or real
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
  
  
