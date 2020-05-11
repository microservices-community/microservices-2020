---
title: Contact
layout: page
# feature_image: "bg-2.jpg"
# image_source: "Christian Tomasi"
---

<form class="form-horizontal" action="https://formspree.io/marco.prandini@unibo.it" method="POST">
  <input type="text" name="name" placeholder="Your name">
  <input type="email" name="email" placeholder="Your email (required)" required="required">
  <input type="text" name="subject" value="[Microservices 2020]">
  <textarea name="message" placeholder="Your message"></textarea>
  <label for="confirmation"><input type="checkbox" id="confirmation" name="confirmation" value="confirmation" required="required" />
    Consent in terms of data-protection law: I hereby consent that my data may be collected, stored and used as described in the procedure <a href="{{ '/gdpr_contact/' | relative_url }}" target="_blank">"Microservices 2020: Contacting"</a>. I can revoke this consent at any given time without giving any reason. Moreover, I can claim information as to the stored data and require correction, deletion and inhibition of my personal data.
  </label>
  <br>
  <button class="btn btn-primary" type="submit">Submit message</button>
</form>
