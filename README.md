kontak
======

&lt;?php $field_name = $_POST['cf_name']; $field_email = $_POST['cf_email']; $field_message = $_POST['cf_message'];  $mail_to = 'servasiussuwaldussitu@gmail.com'; $subject = 'Message from a site visitor '.$field_name;  $body_message = 'From: '.$field_name."
"; $body_message .= 'E-mail: '.$field_email."
"; $body_message .= 'Message: '.$field_message;  $headers = 'From: '.$field_email."
"; $headers .= 'Reply-To: '.$field_email."
";  $mail_status = mail($mail_to, $subject, $body_message, $headers);  if ($mail_status) { ?> 	&lt;script language="javascript" type="text/javascript"> 		alert('Thank you for the message. We will contact you shortly.'); 		window.location = 'contact_page.html'; 	&lt;/script> &lt;?php } else { ?> 	&lt;script language="javascript" type="text/javascript"> 		alert('Message failed. Please, send an email to servasiussuwaldussitu@gmail.com'); 		window.location = 'contact_page.html'; 	&lt;/script> &lt;?php } ?>
