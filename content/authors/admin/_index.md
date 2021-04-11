---
# Display name
title: Stephanie M Garcia

# Username (this should match the folder name)
authors:
- admin

# Is this the primary user of the site?
superuser: true

# Role/position
role: Texts & Technology PhD Student

# Organizations/Affiliations
organizations:
- name: University of Central Florida
  url: ""

# Short bio (displayed in user profile at end of posts)
bio: My research interests include the effects of intersectional feminism on the audeince perception of Graphic Novels.

interests:
- LGBTQIA+ representation 
- Media Studies
- Narrative

education:
  courses:
  - course: PhD in Texts & Technology
    institution: University of Central Florida
    year: 2025 
  - course: MA in Interdisciplinary Studies
    institution: University of Central Florida
    year: 2019
  - course: BS in Psychology
    institution: University of Central Florida 
    year: 2014

# Social/Academic Networking
# For available icons, see: https://sourcethemes.com/academic/docs/page-builder/#icons
#   For an email link, use "fas" icon pack, "envelope" icon, and a link in the
#   form "mailto:your-email@example.com" or "#contact" for contact widget.
social:

- icon: linkedin
  icon_pack: fab
  link: https://www.linkedin.com/in/smargar/
- icon: github
  icon_pack: fab
  link: https://github.com/smargarink

- icon: cv
  icon_pack: ai
  link: files/cv.pdf

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ""

# Organizational groups that you belong to (for People widget)
#   Set this to `[]` or comment out if you are not using People widget.
user_groups:
- Researchers
- Visitors
---

Stephanie Garcia is a Texts and Technology student that specializes in Digital Humanities. Prior to joining T&T, Stephanie earned a Masters of Arts in Interdisciplinary Studies focusing in Cognitive Science and Emerging Media. She is a triple Knight and also received her Bachelors of Science in Psychology from UCF. Her research interests are gender representation in media and the roles women, especially women of color, play in digital media. Her other research interests focus on cultural representation and trends in the arts, specifically how cultural trends are perpetuated through media and vise versa.

	$(document).ready(function(){
		var quoteSource=[
		{
			quote: "You miss 100% of the shots you don’t take. - Wayne Gretzky",
      name: "Michael Scott"
	    },
	    {
	    	quote:"Do I need to be liked? Absolutely not. I like to be liked. I enjoy being liked. I have to be liked. But it’s not like this compulsive need like my need to be praised.",
	    	name:"Michael Scott"
	    },
	    {
	    	quote:"I am fast. To give you a reference point I am somewhere between a snake and a mongoose… And a panther.",
	    	name:"Dwight Shrute"
	    },
	    {
	    	quote:"Through concentration, I can raise and lower my cholesterol at will.",
	    	name:"Dwight Shrute"
	    },
	    {
	    	quote:"Sometimes I’ll start a sentence and I don’t even know where it’s going. I just hope I find it along the way.",
	    	name:"Michael Scott"
	    },
	    {
	    	quote:"I talk a lot, so I’ve learned to tune myself out.",
	    	name:"Kelly Kapoor"
	    },
	    {
	    	quote:"If I don’t have some cake soon, I might die.",
	    	name:"Stanley Hudson"
	    },
	    {
	    	quote:"I just want to lie on the beach and eat hot dogs. That’s all I’ve ever wanted.",
	    	name:"Kevin Malone"
	    },
	    {
	    	quote:"There’s a lot of beauty in ordinary things. Isn’t that kind of the point?",
	    	name:"Pam Beesly"
	
	    }

	];
		

		$('#quoteButton').click(function(evt){
			//define the containers of the info we target
			var quote = $('#quoteContainer p').text();
			var quoteGenius = $('#quoteGenius').text();
			//prevent browser's default action
			evt.preventDefault();
			//getting a new random number to attach to a quote and setting a limit
			var sourceLength = quoteSource.length;
			var randomNumber= Math.floor(Math.random()*sourceLength);
			//set a new quote
			for(i=0;i<=sourceLength;i+=1){
			var newQuoteText = quoteSource[randomNumber].quote;
			var newQuoteGenius = quoteSource[randomNumber].name;
			//console.log(newQuoteText,newQuoteGenius);
      var timeAnimation = 500;
      var quoteContainer = $('#quoteContainer');
      //fade out animation with callback
      quoteContainer.fadeOut(timeAnimation, function(){
        quoteContainer.html('');
				quoteContainer.append('<p>'+newQuoteText+'</p>'+'<p id="quoteGenius">'+'-								'+newQuoteGenius+'</p>');
        //fadein animation.
        quoteContainer.fadeIn(timeAnimation);
      });  
			
			break;
		};//end for loop
	
	});//end quoteButton function
		
		
});//end document ready

