This is still a work in progress, but it should work just fine. Let me know if you notice any issues. 

### Usage 
First, include the class in your project. 

`require 'Envato_marketplaces.php';`

Next, create a new instance of the class:

`$Envato = new Envato_marketplaces();`

And that's really it. You now have access to all of the available functions. 

### Examples (to be updated)
#### Search for Sliders Across all Marketplaces
    $Envato = new Envato_marketplaces();
    $sliders = $Envato->search('sliders');
    $Envato->prettyPrint($sliders);

##### Limit results to a particular site...
    $Envato = new Envato_marketplaces();
    $sliders = $Envato->search('sliders', 'codecanyon');
    $Envato->prettyPrint($sliders);

##### Limit further to a marketplace category...
   $Envato = new Envato_marketplaces();
    $sliders = $Envato->search('sliders', 'codecanyon', 'plugins');
    $Envato->prettyPrint($sliders);

#### Get Account Balance
    $Envato = new Envato_marketplaces();
    $Envato->set_api_key('your api key');
    $vitals = $Envato->private_user_data('your username', 'vitals');

    # Display array for review
    $Envato->prettyPrint($vitals);

   # Echo Balance
   echo $vitals->balance;

#### Get Featured Item
    require 'Envato_marketplaces.php';
    $Envato = new Envato_marketplaces();
    $featured = $Envato->featured('codecanyon');

    # Just for reviewing available props
    $Envato->prettyPrint($featured);

    # Featured author
    echo $featured->featured_author->user;

    # Featured file
    echo $featured->featured_file->url;

    #Free file
    echo $featured->free_file->url;



   

