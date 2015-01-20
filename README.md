# Scraping
<!DOCTYPE html>
<html>
<center> 
<head><link href="style.css" rel="stylesheet" /> #LGBT Tweets</head>
    <title>Gay Rights Revolution</title>
<link href='http://fonts.googleapis.com/css?family=Yanone+Kaffeesatz' rel='stylesheet' type='text/css'>
	<meta name="description" content="A page of pangrams" />
    <meta name="author" content="Your Name" />
    <meta name="keywords" content="pangram, quick foxes, educational">

<!--Load the AJAX API-->
    <script type="text/javascript" src="https://www.google.com/jsapi"></script>
    <script type="text/javascript">
    // Load the Visualization API and the core charts package.
    google.load('visualization', '1.0', {
        'packages': ['corechart']
    });

    // Set a callback to run when the Google Visualization API is fully loaded.
    google.setOnLoadCallback(getData);

    function getData() {
        // this is the key for the spreadhseet with your data in it, you can copy this from the URL for the sheet
        var key = "11M__zqM32g1l8FYnIFoXy1T2PalLCPHNFMMiBjxUmco";
        // this is the range in the sheet to find the data
        var range = "A2:B25";
        // get the date from the range specified
        var query = new google.visualization.Query('https://docs.google.com/spreadsheet/ccc?key=' + key + '&usp=sharing&range=' + range);
        // Send the query with a callback function, to be executed when the data is reeady
        query.send(drawChart);
    }

    // Callback that creates and populates a data table,
    // instantiates the line chart, passes in the data and
    // draws it.
    function drawChart(response) {

        // standard bit of code in case we are offline or you deleted the google sheet or something like that
        if (response.isError()) {
            console.log('Error in query: ' + response.getMessage() + ' ' + response.getDetailedMessage());
            return;
        }

        // dig out the data from the response to the query 
        var data = response.getDataTable();
        // there are squillions of cool options for your charts, shove them into this JSON object
        // read more https://developers.google.com/chart/interactive/docs/gallery/linechart
        var options = {
            'title': 'Tweet Volume By Hour (January 7 14:30 - January 8 14:30)',
            'width': 1000,
            'height': 400,
            'legend': { position: 'in'}
        };

        // Instantiate and draw our line chart, passing in the options JSON object.
        var chart = new google.visualization.LineChart(document.getElementById('chart_div'));
        chart.draw(data, options);
    }
    </script>
</head>



<body>
<div id="outer"> 
	<div id="text">
	<h1>The Growing Momentum of Gay Rights #LGBT </h1>
		<h2>The United States have seen a sweep of courts knocking down gay marriage ban in 36 states</h2>
	<span class="highlight"> </span`>
	<img src="images/gayflag.jpg">
	
	<P class="breakout-box">Gay flag representing gay rights.</p>
	
	<p>Gay marriage has grown very popular within the western world and is continueing to grow year by year. Gay marriage is sweeping across America, especially since the United States Supreme Court (SCOTUS) have decided to pick up the case this year and decide once and for all if gay and lesbians havea constitutional right to marry. To show the popularity of gay rights triumphing in the world, I scraped data from twitter.

    Here is the twitter trend #LGBTtracked for 24 hours from January the 7th till the 8th.</p>
	<p>The tweeets were tracked and scraped using pyhton and running the programme through the computer terminal.</p>
	<p>The data gathered through twitter ran continuosly for 24 hours without any problems. The tweet #LGBT seemed very popular in my data peaked around the 18 hour mark of my scraping data at 1248 tweets in an hour. In the beginning my data was rather slow with incoming tweets, but after the 10 hour mark there was an increase in tweets mentioning #LGBT. I also scraped the following hashtags #gay and #equality, but after analysing those tweet I found some negative associates within one tweet and the other wasn't just about gay rights. I wanted to focus mainly on the success of gay, lesbian, bisexual, and transgendered invidivuals. </p>

    <p> In my visualization process of my graph I decided to delete a weeks worth of data and focus on 24 hours worth of tweets to compress the information into tweets by hour. I used approximately 17,288 tweets for my data. I tried using a weeks worth of tweets, but ran into some complications. It was very complicated to maneuver into an excel sheet. The issue I had was tryinh to alter 150,000 tweets, which resulted in microsoft excel crashing and not responding to commands.</p>
	
	    <!--Div that will hold the pie chart-->
    <div id="chart_div"></div>

    <p> Here is a view of data scraped and saved into a CSV file and stored within the university server. I then cleaned up the data by deleting bugged tweets from the CSV file. I used =MID function to caculate the tweets per hour for each individual tweet. After this process i then created a pivot table for my data and simplified my tweets per hour and transferred the data into a google spreadsheet.

    <p> The complicated issue with handling this data was to remove the bugs that occurred within the excell sheet. Some tweets were bugged which took a considerate amount of time to remove. </P>
	<div id="menu">

		<img href="http://s29.photobucket.com/user/aceflash111/media/ScreenShot2015-01-20at120826.png.html" target="_blank"><img src="http://i29.photobucket.com/albums/c298/aceflash111/ScreenShot2015-01-20at120826.png" border="0" alt=" photo ScreenShot2015-01-20at120826.png"/></a>
       
<p> My data is very accurate and was scraped using python and accessing the data using the terminal. I believe the bst possible interpretations and practical uses of the visualization is to show the popularity of the growing gay rights movement and who supports it. If my data was gathered and recieved far fewer tweets then what i achieved then i could conclude many individuals do not support LGBT rights, but since they I recieved quantom amounts of data, I can assume many individuals support someones right to marry. longer down the line if I could focus my tweets by region I could also possibly acknoweldge the popularity and rights of gay individuals in those areas. An example would be a comparison of LGBT tweets of The United Kingdom compared to Uganda's region of tweets on the same issue. </p>


<p> below are a few links that focus on LGBT issues around the world and help spread the issues dealing with gay rights.
           <li><a href="http://gaystarnews.com">GayStarNews</a>
           <li><a href="http://www.huffingtonpost.com/gay-voices/">HuffingtonPost</a>
           <li><a href="http://www.pinknews.co.uk/home/">PinkNews</a>
    </div>
    <a href="https://twitter.com/share" class="twitter-share-button" data-via="JoshBosh11">Tweet</a>
<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+'://platform.twitter.com/widgets.js';fjs.parentNode.insertBefore(js,fjs);}}(document, 'script', 'twitter-wjs');</script>

<a target="_blank" title="find us on Facebook" href="http://www.facebook.com/joshua.poncil"><img alt="follow me on facebook" src="//login.create.net/images/icons/user/facebook_40x40.png" border=0></a>


	</div>
</div>
</body>
</center>
</html>
