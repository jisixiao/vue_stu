<template>
    <section id="contact" class="section-wrapper contact-section" data-stellar-background-ratio="0.5">
      <div class="parallax-overlay"></div>
      <div class="container">
        <div class="row">

          <!-- Section Header -->
          <div class="col-md-12 col-sm-12 col-xs-12 section-header wow fadeInDown section-header-parallax">
            <h2><span class="highlight-text">Contact Us</span></h2>
            <p class="col-md-8 col-sm-10 col-xs-12 col-md-offset-2 col-sm-offset-1">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quod, nam corporis quas, saepe minima error aperiam dolorum aliquam, quis deserunt eos eius quisquam odio itaque in minus distinctio dolores ipsam.</p>
          </div>
          <!-- Section Header End -->

          <div class="contact-details">


            <!-- Contact Form -->
            <div class="col-sm-offset-3 col-md-6 col-sm-6 col-xs-12 contact-form wow bounceInRight">

              <!--NOTE: Update your email Id in "contact_me.php" file in order to receive emails from your contact form-->
              <form name="sentMessage" id="contactForm"  novalidate>
                <div class="control-group">
                  <div class="controls">
                    <input type="text" class="form-control"
                           placeholder="Full Name" id="name" required
                           data-validation-required-message="Please enter your name" />
                    <p class="help-block"></p>
                  </div>
                </div>
                <div class="control-group">
                  <div class="controls">
                    <input type="email" class="form-control" placeholder="Email"
                           id="email" required
                           data-validation-required-message="Please enter your email" />
                  </div>
                </div>

                <div class="control-group">
                  <div class="controls">
	<textarea rows="10" cols="100" class="form-control"
            placeholder="Message" id="message" required
            data-validation-required-message="Please enter your message" minlength="5"
            data-validation-minlength-message="Min 5 characters"
            maxlength="999" style="resize:none"></textarea>
                  </div>
                </div>
                <div id="success"> </div> <!-- For success/fail messages -->
                <div class="text-center"><button type="submit" class="btn btn-primary">Submit Message</button></div>
              </form>
            </div>

          </div>
        </div>
      </div>
    </section>

</template>



