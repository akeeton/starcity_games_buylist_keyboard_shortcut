# starcity_games_buylist_keyboard_shortcut

This is a simple Javascript bookmarklet that makes using the [Star City Games buylist](http://www.starcitygames.com/buylist/) much easier and faster.  Press the backtick (`)/tilde (~) key to put the cursor in the search box and clear it.

## Usage

1. Create an empty bookmark and input the following condensed Javascript code as the URL.

    javascript:(function()%7Bdocument.onkeypress %3D function onKeypressGiveSearchBarFocus(event) %7Bvar KEY %3D 96%3B %2F* %60 (backtick) *%2Fif (event.which %3D%3D KEY) %7B%24('%23bl-search-name-text').focus().val('')%3Bevent.preventDefault()%3B%7D%7D%7D)()
    
2. Go to http://www.starcitygames.com/buylist.

3. Enter a card name in the "Product Name" search bar.

4. Press the backtick (`)/tilde (~) key to clear the search bar and give it focus.

## Javascript source

    document.onkeypress = function onKeypressGiveSearchBarFocus(event) {
	    var KEY = 96; /* ` (backtick) */
    
	    if (event.which == KEY) {
		    $('#bl-search-name-text').focus().val('');
		    event.preventDefault();
	    }
    };

https://mrcoles.com/bookmarklet was used to create the bookmarklet.
