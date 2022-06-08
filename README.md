# play14-website

Main website for play14.org  
This site contains all the information about what **#play14** is and is not, past and future **#play14** events, players, games played and much more.  
This website is powered by [Jekyll](https://jekyllrb.com/) and is hosted on [GitHub Pages](https://pages.github.com/).

You can find more information on Jekyll and the different syntaxes/technologies it uses in the following list

- [Jekyll Tips](http://jekyll.tips/)
- [Front Matter](https://jekyllrb.com/docs/frontmatter/)
- [YAML](http://yaml.org/)
- [Liquid template engine](https://github.com/Shopify/liquid)
- [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Run the website in development mode

To run the website locally in development mode, you need to

- Install [Jekyll](https://jekyllrb.com/docs/installation/)
- Clone or fork the [GitHub repository](https://github.com/play14team/play14-website)
- Open a command prompt from the directory containing the clone of `play14-website`
- Run the command `jekyll serve`
- Navigate to the URL provided, usually `http://127.0.0.1:4000`

## Contribute content

You can start contributing content by creating a [pull request](https://yangsu.github.io/pull-request-tutorial/) on our [GitHub repository](https://github.com/play14team/play14-website).

Blog posts, Games and Events are all written in [Markdown](https://daringfireball.net/projects/markdown/) using Jekyll's [YAML Front Matter](https://jekyllrb.com/docs/frontmatter/).

Directory structure

- Events markdown files should be placed into the [\_events](_events) directory.
  - The file name should respect the template `<yyyy-mm>.md`.
  - Events images should be placed into the `images/events/<event-name>` sub-directory. Their size should be 600x500.
- Games markdown files should be placed into the [\_games](_games) directory.
  - The file name should respect the template `<game-name>.md`.
  - Game images should be placed into the `images/games/<game-name>` sub-directory. Their size should be 800x533.
  - Game files should be placed into the `files/<game-name>` sub-directory.
- Players makrdown files should be placed into [\_players](_players) directory.
  - The file name should respect the template `<firstname>-<lastname>.md`
  - Player picture should be placed into the `images/players` sub-directory. Their it's size should be 500x500.
- Posts markdown files should be placed into the [\_posts](_posts) directory.
  - The file name should respect the template `<yyyy-mm-dd-post-title>.md`.
  - Post images should be placed into the `images/posts` sub-directory. Their size should be 800x533.

You might need to add extra data in one of the following YAML files in the [\_data](_data) directory.

- [location.yml](_data/locations.yml) contains the list of recurring event locations
- [sponsors.yml](_data/sponsors.yml) contains the list of all sponsors

You should NOT have to modify any other directory or file.
You can find more information on how to write a blog post with Jekyll [here](https://jekyllrb.com/docs/posts/)

## Event Front Matter metadata

Here is an example of the metadata you can provide in the [Front Matter](https://jekyllrb.com/docs/frontmatter/) part of an event file using [YAML](http://yaml.org/).

```yaml
layout: event # layout should always be 'event'

title: Luxembourg 2017 # default is location and year of the event
category: luxembourg # the location of the event in lowercase, used to filter on the events list

schedule:
  dates: March 23-25 2017 # dates that are displayed on the site
  start: 2017-03-23 18:30:00 # actual start date and time
  finish: 2017-03-25 17:00:00 # actual finish date and time
  isCancelled: false # indicator whether the event is cancelled (true/false)

location:
  name: Technoport # name of the location
  area: Esch/Belval # area of the location
  address: > # address of the location
    9, avenue des Hauts-Fourneaux
    L-4362 Esch-sur-Alzette
  url: http://www.technoport.lu # website of the location
  map: https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d20723.71349371132!2d5.964228003547424!3d49.51351172884244!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xe8b8bed0e26f33a!2sTechnoport+S.a.!5e0!3m2!1sen!2slu!4v1480793868583 # embedded URL from Google Maps (needs to be copied without the iframe HTML code, only the URL)

images: # images of the location or any other image of the event (size 600x500)
  - /images/events/luxembourg/01.jpg
  - /images/events/luxembourg/02.jpg

members: # organization team members,values should match the name of a player MD file from _players folder
  - Cédric Pontet
  - Diego De Biasio
  - Pierre Neis
  - Yann Gensollen

redirect_from:
  - /luxembourg # used so that people can reach your page by typing the url 'play14.org/<location>' (unique for the whole site, only for events that are not over)

sponsors: # sponsors of your event
  - name: Agile Partner # name of the sponsor, should match the name of a sponsor in the _data/sponsors.yml file (if your sponsor does not exist, you need to create it in the yaml file)
    type: Gold Sponsor # category of your sponsor, sponsors will be automatically grouped by category
  - name: Technoport
    type: Gold Sponsor
  - name: AIGLU
    type: Organization & Support
  - name: Marmelab
    type: Organization & Support
  - name: We&Co
    type: Organization & Support
```

The rest of the file is written as plain [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### Registration

There are different way to integrate a registration form on the website, depending on the ticketing system you are using.

#### Link registration

The simplest way to integrate registration is to provide the URL to any external system that will handle registration. When clicking the _Register_ button on the event web page, it will open a new tab pointing to the given URL.

```yaml
registration:
  type: link
  url: https://play14-luxembourg2017.eventbrite.com
```

#### Form registration

You can also integrate a registration form directly into the event page. To do that, you first need to declare the type of registration in the Front Matter YAML section.

```yaml
registration:
  type: form
```

Then you simply add the form (code usually generated by your ticketing system) in as plain HTML in the Markdown section of the page.

One important thing is to put a `title="Registration"` attribute to the _anchor_ tag so that, when clicking on the _Register_ button, the page will be automatically scolled down to the registration form.

```markdown
## Registration

<a title="Registration" href="https://www.weezevent.com/?c=sys_widget" class="weezevent-widget-integration" target="_blank" data-src="https://www.weezevent.com/widget_billeterie.php?id_evenement=323358&lg_billetterie=2&code=42627&resize=1&width_auto=1&color_primary=00AEEF" data-width="650" data-height="600" data-id="323358" data-resize="1" data-width_auto="1" data-noscroll="0" data-nopb="0">Registration</a><script type="text/javascript" src="https://www.weezevent.com/js/widget/min/widget.min.js"></script>
```

#### Weezevent registration

When the chosen ticketing platform is [Weezevent](https://weezevent.com/), we implemented a specific integration to simplify things.

All you need to do is define the type of integration as `weezevent` in the Front Matter YAML and then specify the `eventId` and `code` that are provided by Weezevent when generating a widget.

The values can be found in the URL in the `data-src` attribute of the widget.

```
data-src="https://www.weezevent.com/widget_billeterie.php?id_evenement=323358&lg_billetterie=2&code=42627&resize=1&width_auto=1&color_primary=00AEEF"
```

The Front Matter YAML should look like that:

```yaml
registration:
  #type of registration should be weezevent
  type: weezevent
  #the value of the id_evenement URL parameter
  eventid: 374193
  #the value of the code URL parameter
  code: 16876
```

#### Eventbrite registration

When the chosen ticketing platform is [Eventbrite](https://www.eventbrite.com/), we implemented a specific integration to simplify things.

```yaml
registration:
  #type of registration should be eventbrite
  type: eventbrite
  #the id of your event on Eventbrite
  eventid: 64806410719
```

## Game Front Matter metadata

Here is an example of the metadata you can provide in the [Front Matter](https://jekyllrb.com/docs/frontmatter/) part of an event file using [YAML](http://yaml.org/).

```yaml
layout: game # layout should always be 'game'

title: "X + Y game" # the title of the game
category: game # the type of game in lowercase (game, icebreaker, warmup), used to filter on the games list
tags: # some of the values / learning objectives of the game
  - trust
  - empathy
  - zoom out
  - collaboration
  - competitive

authors: # the list of people who wrote the game documentation down (should match the 'name' of a player in the directory _players)
  - Chris Caswell
originators: # the list of people who originally proposed the game (should match the 'name' of a player in the directory _players)
  - Leon-Cosmin Lupu
  - Dragos Marius Jumanca
firstplayed: Luxembourg 2015 # the first event the game was played at (should match the 'title' of an event in the directory _events)
scale: Min 6, Max 16 # indicates the min/max number of people for the game
timebox: 30-45 mins # indicates the min/max timebox for the game

# a description for the game, that will appear as a summary
description: We have a natural tendency to optimise the world immediately around us and focus on personal or team success. Often this can be to the detriment of others  and the wider organisation which ultimately affects their success. This game exploits this aspect of human nature to demonstrate that localised sub-optimisation can have a dramatic effect when we look at the bigger picture.

materials: # materials that are necessary to play the game
  - TV or Projector
  - Board or Flipchart and pens
  - Post it notes
  - Timer
  - Game board and scoring chart

resources: # internal / external resources needed to play the game
  - name: Game board # name of the resource
    url: /files/x-y-game/x-y-game-board.xlsx # url to the resource

preparations: # preparations you should do before you can play the game
  - Print copies of the scoring chart
  - Make a simple decision board for each department to indicate the option they’ve chosen (E.G. | Team name | Decision X or Y | )
  - Two post its per team, one with X and the other with Y

safety: # some safety warnings for some games that can trigger mixed feelings/reactions amongst participants
  - title: Stress
    description: This game is highly valuable and educational, but to achieve this it creates an environment of stress, frustration and conflict. Be sure that is it safe for your team to experience these emotions and take the time to follow this game with a team building exercise.
  - title: Christmas Bonus
    description: Use a box of chocolates as the “Christmas Bonus” in this game, and when nobody actually wins (company has failed) at the end of game, share the chocolates during the reflection to begin to defuse.

images: # images illustrating the game (size 800x533)
  - /images/games/x-y-game/01.png
```

The rest of the file is written as plain [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

Common headers should be

- HOW TO PLAY
  - SETUP
  - GOAL
  - RULES
- FACILITATION
- REFLECTIONS
- TAKEAWAYS
