FOR PRIVACY AND CODE PROTECTING REASONS THIS IS A SIMPLIFIED VERSION OF CHANGES AND NEW FEATURES

TASK DATE: 27.10.2017 - FINISHED: 27.10.2017

TASK LEVEL: (EASY)  

TASK SHORT DESCRIPTION: 1133 (bootstrap icon colour to change according to hex used for 'theme text colour')

GITHUB REPOSITORY CODE: hotfix/task-1133-bootstrap-icon-colour-to-change


CHANGES
 
	IN FILES: 
	
		index.php
		
			ADDED CODE: 
			
                <li>
                    <a href="{{ url:site uri='users/logout' }}">
                        <div class="row">
                            <div class="col-md-3 col-sm-3"><span class="glyphicon glyphicon-log-out" style="color: #36454f !important; font-size: 24px; -webkit-text-stroke: 2px #f2f2f2; margin-left: 7px;"></span></div>
                            <div class="col-md-9 col-sm-9">Logout</div>
                        </div>
                    </a>
                </li>				
	
	
	
	
		header.html
		
			ADDED CODE: 
			
				<?php
					//Set some common used variables
					$equal_colours = (Settings::get('theme_colour') == Settings::get('theme_menu_text_colour'))
												? Settings::get('theme_colour')
												: Settings::get('theme_menu_text_colour');
												
					if  (Settings::get('theme_colour') != Settings::get('theme_menu_text_colour')) {
						$not_equal_colours = Settings::get('theme_menu_text_colour');
					}
				?>		
			
			CHANGED CODE about at 30-places
			
				TO: "color: <?php echo $equal_colours ?> !important;" //I changed the lot IF statement to ONE
			
		
		
		
		
		\menu.css
		
			ADDED CODE: 
			
				div.non-profile-img {
					display: block;
					height: 27px;
					width: 27px;	
					margin-top: -3px;
					padding-top: 2px;
					background-color: transparent;
					border: 2px solid;
					border
					border-radius:50%;
					-moz-border-radius:50%;
					-webkit-border-radius:50%;	
				}
