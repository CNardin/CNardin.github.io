---
title: Contact
type: landing

sections:

  - block: markdown
    content:
      text: |
 
            <div class="col-12 col-lg-4 section-heading">
                <h2>Contact</h2>    
            </div>           
                

            <div class="mb-3">
            <form method="POST" name="contact"><input type="hidden" name="form-name" value="contact">
                <div class="form-group form-inline">
                <label class="sr-only" for="inputName">Name</label>
                <input type="text" name="name" class="form-control w-100" id="inputName" placeholder="Name" required="">
                </div>
                <div class="form-group form-inline">
                <label class="sr-only" for="inputEmail">Email</label>
                <input type="email" name="email" class="form-control w-100" id="inputEmail" placeholder="Email" required="">
                </div>
                <div class="form-group">
                <label class="sr-only" for="inputMessage">Message</label>
                <textarea name="message" class="form-control" id="inputMessage" rows="5" placeholder="Message" required=""></textarea>
                </div>
                <button type="submit" class="btn btn-outline-primary px-3 py-2">Send</button>
            </form>
            </div>
            

            <ul class="fa-ul">                
            
            <li>
                <i class="fa-li fas fa-map-marker fa-2x" aria-hidden="true"></i>
                <span id="person-address">Wolfgang-Pauli-Strasse, 8049 Zürich</span>
            </li>

            <li>
                <i class="fa-li fab fa-github fa-2x" aria-hidden="true"></i>
                <a href="https://github.com/cnardin" target="_blank" rel="noopener">Our code</a>
            </li>                                   
            
            <li>
                <i class="fa-li fas fa-envelope fa-2x" aria-hidden="true"></i>
                <a href="/">mailto:cnardin@ethz.ch</a>
            </li>
            
            </ul>

            
            <div class="d-none">
                <input id="map-provider" value="1">
                <input id="map-lat" value="47.40878965736161">
                <input id="map-lng" value="8.5071705404044">
                <input id="map-dir" value="Wolfgang-Pauli-Strasse, 8049 Zürich">
                <input id="map-zoom" value="15">
                <input id="map-api-key" value="AIzaSyCA3WRcrUWprPLefbiLa0FiS5AJymB8DOU">
            </div>

---
