## Contact Us

<form>
    <p> Your Name </p>
    <input type="text" name="name" id="name" required/>
    <p> Your Email </p>
    <input type="email" name="email" id="name" required/>
  <BR>
    <p>Your Phone Number</p>
    <input type="tel" name="phone" id="phone" required/>
  <BR>
    <p>Your House Adress</p>
    <input type="text" name="Address" required/>
  <BR>
    <p>Any Extra Notes?</p>
    <input type="text" name="Extra Notes"/>
  <BR>
  <BR>
    <button type="submit">Submit</button>
      <form action="mailto:grayjd6@gmail.com">
</form>
  
<form method="post" action="grayjd6@gmail.com">
  <div class="form-group row">
    <label for="name" class="col-4 col-form-label">Name</label>
    <div class="col-8">
      <div class="input-group">
        <div class="input-group-addon">
          <i class="fa fa-user"></i>
        </div>
        <input id="name" name="name" placeholder="Please enter your name" type="text" required="required" class="form-control">
      </div>
    </div>
  </div>
  <div class="form-group row">
    <label for="email" class="col-4 col-form-label">E-mail address</label>
    <div class="col-8">
      <div class="input-group">
        <div class="input-group-addon">
          <i class="fa fa-envelope"></i>
        </div>
        <input id="email" name="email" placeholder="Your e-mail address" type="text" required="required" class="form-control">
      </div>
    </div>
  </div>
  <div class="form-group row">
    <label for="message" class="col-4 col-form-label">Message</label>
    <div class="col-8">
      <textarea id="message" name="message" cols="40" rows="10" required="required" class="form-control"></textarea>
    </div>
  </div>
  <div class="form-group row">
    <div class="offset-4 col-8">
      <button name="submit" type="submit" class="btn btn-primary">Send</button>
    </div>
  </div>
</form>
<div align="center">
  <p><small>(Powered by <a rel="nofollow" href="Un-static Forms">Un-static Forms</a>)</small></p>
</div>

    <?php
    $content= "First Name: ".$_POST['firstname']."\n";
    $content.= "Last Name: ".$_POST['lastname']."\n";   

    $to = "grayjd6@gmail.com" ;               

            $headers .= "MIME-Version: 1.0\n";
            $headers .= "Mailed-By: test.com\n";
            $headers .= "Content-Type: text/HTML; charset=ISO-8859-1\n";            

            $headers = 'From:'.$_POST['email']  . "\r\n" .'Reply-To:'.$_POST['email'] . "\r\n" .'X-Mailer: PHP/' . phpversion(); 

            if(mail($to,'testsubject',$content,$headers)){
            ?>
            <script type="text/javascript">
                    alert("Thank you for contacting us.We will get back to you soon.");
                    window.location.href="index.php";
            </script>
            <?php
            }else{
            ?>
            <script type="text/javascript">
                    alert("mail not sent! Please try after some time!");
                    window.location.href="index.php";
            </script>
            <?php

            }
    ?>
      
[Back](index.md)
