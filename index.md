---
layout: workshop
venue: "University at Buffalo, SUNY"   # brief name of host site without address (e.g., "Euphoric State University")
address: "University at Buffalo, SUNY, North Campus"     # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "United States"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
latitude: "43.002890"     # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-78.788780"    # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "June 11-23, 2023"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00 am - 5:00 pm EDT"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2023-06-11      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2023-06-23        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Alexey Akimov", "Graham Worth", "Michael Filatov", "Niri Govind", "Daniel Mejia Rodriguez", "Micheline Soley" ]  # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: [ "Qingxin Zhang", "Mohammad Shakiba", "Eryn Spinlove", "Konstantin Komarov", "Edoardo Apra" ] # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["alexeyak@buffalo.edu"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:         # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
googleform: https://forms.gle/XLwU2DFGbBgBXeto6
carpentry: "sc"
---


{% comment %}
root: .  # Is the only page that doesn't follow the pattern /:path/index.html
permalink: index.html  # Is the only page that doesn't follow the pattern /:path/index.html
{% endcomment %}


# Excited States and Nonadiabatic Dynamics CyberTraining Workshop 2023

## About the Summer School and Workshop

The CyberTraining workshop aims to educate graduate students, postdocs, researchers, and educators working in a 
broader field of nonadiabatic and excited-state dynamics as well as in computational material sciences in a variety
of tools and methods for such types of calculations. The workshop will provide conceptual and practical hands-on 
training in a range of methods and cyberinfrastructure (software and platforms) for modeling excited state and 
nonadiabatic dynamics in abstract models and atomistic materials. We will also cover tools and workflows for 
building atomistic models, computing excited states of molecular and periodic systems, as well as pre- and post-processing 
operations, and data analysis. 

Participants not only will learn about using the tools but will be exposed to the underlying machinery 
of such methods and will be familiarized with their development. The programming-driven nature of the school will
help the participants to go beyond the standard computational chemistry curriculum. The workshop will culminate with 
a capstone project presentation, through which the participants will demonstrate their ability to leverage the new tools 
in their active research. 

Keywords and topics:

- nonadiabatic dynamics
- excited states
- quantum dynamics
- quantum-classical methods
- charge transfer
- excitation energy transfer
- trajectory surface hopping
- exact factorization
- TD-DFT, CASSCF, GW/BSE
- algorithms and methods
- software, programming, Python
- best practices, Git, GitHub

 
The school aims to provide training in a range of advanced tools for excited state and 
nonadiabatic molecular dynamics calculations. 
This year, the focus will be on the following packages:

- Libra (Akimov)
- Quantics/MCTDH (Worth)
- GAMESS (Filatov)
- NWChem (Govind)
- TT-SOFT, TT-Chebyshev (Soley)

The school will leverage the [OnDemand](https://ondemand.ccr.buffalo.edu) gateway at the University at Buffalo


## Logistics

{% if page.humandate %}
<p id="when">
  <strong>When:</strong>             
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% if page.latitude and page.longitude %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latitude}}&mlon={{page.longitude}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latitude}},{{page.longitude}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
CONTACT EMAIL ADDRESS
Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

### Schedule

{% include base_path.html %}

The details may vary and the order of topics may be changed, the topics may be omitted or added. Please check for the updates. 

  <table class="table table-striped">
  
  <tr>
    <td class="col-md-3"><strong>Date</strong></td>
    <td class="col-md-7"><strong>Topics</strong></td> 
    <td class="col-md-2"><strong>Instructors</strong></td>
  </tr>

  <tr>
    <td class="col-md-3">June 11, 2023 (Day 1), Sunday</td>
    <td class="col-md-7">
      <ul>        
        <li>Arrivals</li>
        <li>Welcome dinner</li>
      </ul>
    </td> 
    <td class="col-md-7">None</td>
  </tr>

  
  <tr>
    <td class="col-md-3">June 12, 2023 (Day 2), <strong>Monday</strong></td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/01-introduction">Worshop Kick Off: goals, logistics, details. Overview of the CCR CyberInfrastructure (30 min)</a></li>
        <li><a href="/_episodes/02-python-git">Working with Git and GitHub. Theory and Hands on (60 min)</a> </li>
        <li><a href="/_episodes/03-libra">General overview of Libra software (Lecture and Demo/Hands on)(90 min)</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/03-libra">Theory of adiabatic and nonadiabatic dynamics. Lecture (60 min)</a></li>
        <li><a href="/_episodes/03-libra">TSH and Ehrenfest dynamics with model Hamiltonians in Libra. Hands on (90 min)</a></li>
        <li><a href="/_episodes/03-libra">HEOM and QTAG in Libra. (60 min)</a></li>
      </ul>
    </td> 
    <td class="col-md-2">Alexey Akimov, Qingxin Zhang, Mohammad Shakiba</td>
  </tr>

  <tr>
    <td class="col-md-3">June 13, 2023 (Day 3), Tuesday</td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/03-libra">Machine learning capabilities of Libra: Lecture, Demo, and Hands on  (60 min)</a></li>
        <li><a href="/_episodes/03-libra">DVR in Libra. Lecture, Demo, and Hands on (90 min)</a></li>
        <li><a href="/_episodes/03-libra">TBD (30 min)</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/03-libra">NA-MD in finite and condensed matter systems with xTB and TD-DFT with Libra/CP2k code. Lecture and Hands on</a></li>
      </ul>
    </td>
    <td class="col-md-2">Alexey Akimov, Qingxin Zhang, Mohammad Shakiba</td>
  </tr>

  <tr>
    <td class="col-md-3">June 14, 2023 (Day 4), Wednesday</td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/04-quantics">Theory and hands on with Quantics and MCTDH</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/04-quantics">Theory and hands on with Quantics and MCTDH</a></li>
      </ul>
    </td>
    <td class="col-md-2">Graham Worth, Eryn Spinlove</td>
  </tr>

  <tr>
    <td class="col-md-3">June 15, 2023 (Day 5), Thursday</td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/04-quantics">Theory and hands on with Quantics and MCTDH</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/04-quantics">Theory and hands on with Quantics and MCTDH</a></li>
      </ul>
    </td>
    <td class="col-md-2">Graham Worth, Eryn Spinlove</td>
  </tr>

  <tr>
    <td class="col-md-3">June 16, 2023 (Day 6), Friday</td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/05-gamess">Theory: Introduction in ensemble DFT and basic aspects of REKS method for ground electronic states</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/05-gamess">Hands on: REKS implementation in GAMESS-US; 
        Demos and practical exercises with REKS method for strongly correlated molecular ground states.</a></li>
      </ul>
    </td>
    <td class="col-md-2">Michael Filatov, Konstantin Komarov</td>
  </tr>
  
  <tr>
    <td class="col-md-3">June 17, 2023 (Day 7), Saturday</td>
    <td class="col-md-7">On your own. Projects time</td>
    <td class="col-md-2"></td>
  </tr>

  <tr>
    <td class="col-md-3">June 18, 2023 (Day 8), Sunday</td>
    <td class="col-md-7">On your own. Projects time</td>
    <td class="col-md-2"></td>
  </tr>

  <tr>
    <td class="col-md-3">June 19, 2023 (Day 9), <strong>Monday</strong></td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/05-gamess">Theory: Ensemble DFT for excited states and its implementation in state-averaged REKS methodology</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/05-gamess">Hands on: Practical exercises with GAMESS-US and NAMD simulations with GAMESS/pyUNI-xMD package</a></li>        
      </ul>
    </td>
    <td class="col-md-2">Michael Filatov, Konstantin Komarov</td>
  </tr>

  <tr>
    <td class="col-md-3">June 20, 2023 (Day 10), Tuesday</td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/06-nwchem">Theory and hands on with NWChem</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/06-nwchem">Theory and hands on with NWChem</a></li>
      </ul>
    </td>
    <td class="col-md-2">Daniel Mejia Rodriguez, Edoardo Apra, Niri Govind</td>
  </tr>

  <tr>
    <td class="col-md-3">June 21, 2023 (Day 11), Wednesday</td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/06-nwchem">Theory and hands on with NWChem</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/06-nwchem">Theory and hands on with NWChem</a></li>
      </ul>
    </td>
    <td class="col-md-2">Daniel Mejia Rodriguez, Edoardo Apra, Niri Govind</td>
  </tr>

  <tr>
    <td class="col-md-3">June 22, 2023 (Day 12), Thursday</td>
    <td class="col-md-7">
      <ul>
        <strong>Morning, 9 am - noon</strong>        
        <li><a href="/_episodes/07-ttsoft">Theory of quantum dynamics with TT-SOFT and TT-Chebyshev, IPA optimization.</a></li>
        <strong>Noon - 1:30 pm</strong> Lunch break
        <strong>Afternoon, 1:30 pm - 5:00 pm</strong>
        <li><a href="/_episodes/07-ttsoft">Hands on with TT-SOFT and TT-Chebyshev, IPA optimization.</a></li>
      </ul>
    </td>
    <td class="col-md-2">Micheline Soley</td>
  </tr>

  <tr>
    <td class="col-md-3">June 23, 2023 (Day 13), Friday</td>
    <td class="col-md-7">Departure.</td>
    <td class="col-md-2"></td>
  </tr>  
  </table>



## Participation
### How to apply to the school

1. Read this page carefully
2. Prepare your application package (you will need it in the next steps)

   2.1. your CV (including graduate or undergraduate GPA)

   2.2. a statement of purpose PDF should describe in no more than 2 pages:

   * your current/ongoing research projects and interests; 
   * how you plan to use the CyberTraining skill gained in this workshop in your research, for instance if you expect using any of the
     packages that will be covered at this workshop (see the agenda);
   * propose at least one potential project to be completed during and shortly after the summer school; the project will be presented shortly after 
     the event (within 1 week). It should leverage one or more tools/software covered during the workshop (see the agenda). The quality and feasibility 
     of the proposed workshop projects will be considered during the selection of the participants. 
         
   2.3. request your advisor to submit a letter of recommendation for you to the following email: "alexeyak AT buffalo DOT edu", 
   please replace "AT" and "DOT" with the corresponding characters

3. Complete the <a href="https://forms.gle/XLwU2DFGbBgBXeto6" target="_blank" rel="nofollow">**Registration form**</a>


### Important Information about your travel

   * The reasonal travel/meal expenses will be covered by the workshop for the domestic applicants
   * Travel expenses for a limited number of international applicants can be covered as well
   * For international applicants: you should be able to enter the US. Visa processing is too lengthy for this planning
   * You will be provided with lodging in a walking distance from the campus
   * UB applicants are also eligible to apply, but your expenses can not be covered by the grant supporting this workshop

### Important dates

   * Workshop application materials are due 5 pm EDT, May 5, 2023
   * Students and Postdocs will be notified of their admission by May 11, 2023
   * Workshop starts: 9 am EDT, June 11, 2023
   * Workshop ends: 5 pm EDT, June 23, 2023


### Who can apply

This summer school is for graduate students, postdocs, and young faculty (and undergraduate in exceptional cases)
working in computational modeling of excited states and nonadiabatic dynamics, both in abstract and atomistic
applications/problems. The school aims to help researchers/students working either in 
methodology development for nonadiabatic or quantum-classical dynamics and in 
applied studies of various types of solar energy materials (photovoltaics, photocatalytics, etc.). 

Postdocs and researchers wishing to acquire the practical experience with new simulation
tools and expand their knowledge in the areas of excited states and nonadiabatic dynamics
are also welcome to participate.


### Selection and restrictions

* **Competitive selection** The applicants will be selected based on the strength of their statement of purpose, as well as the adequate 
  support of their supervisors and their level of fundamental preparation. The lack of training in specialized methods and software is not a problem. 
  What is more important is how ready the applicants are to absorb the new knowlege, how efficiently they can operate during the workshop, 
  and how critical the use of the methods/tools covered in the workshop may be for your future research or career (e.g. educating others). 

* **Capacity.** This year, the event will take place in the in-person format. We will accommodate 20+ in-person participants (excluding instructors).

### Acknowledgement

This workshop is made possible by the NSF-OAC CyberTraining program. Thank you!



{% include links.md %}
