# starcity_games_buylist_keyboard_shortcut

This is a simple Javascript bookmarklet that makes using the [Star City Games buylist](http://www.starcitygames.com/buylist/) much easier and faster.  Press the backtick (`)/tilde (~) key to put the cursor in the search box and clear it.

## Javascript source
    document.onkeypress = function onKeypressGiveSearchBarFocus(event) {
	    var KEY = 96; /* ` (backtick) */
    
	    if (event.which == KEY) {
		    $('#bl-search-name-text').focus().val('');
		    event.preventDefault();
	    }
    };
