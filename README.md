# TRMNL plugins

non-exhaustive collection of open source TRMNL plugins. in sharing these assets we intend to provide transparency in how TRMNL manages user data with respect to 3rd party integrations.

native plugin preview images and configuration options:
[https://usetrmnl.com/integrations](https://usetrmnl.com/integrations)

community Recipes:
[https://usetrmnl.com/recipes](https://usetrmnl.com/recipes)

## Native plugin examples

- [Calendar](/lib/calendar)
- [GitHub Commit Graph](/lib/github_commit_graph)
- [Google Analytics](/lib/google_analytics)
- [Hacker News](/lib/hacker_news)
- [Lunch Money](/lib/lunch_money)
- [Stock Price](/lib/stock_price)
- [Tempest Weather Station](/lib/tempest_weather_station)
- [Weather (generic)](/lib/weather)
- [Days Left Until](/lib/days_left_until)

native plugin structure:

1. file `plugin_name.rb` represents instance of a PluginSetting (user-owned), which belongs to a Plugin (global, immutable)
2. screens are generated by first invoking `Plugins::<PluginName>.new(plugin_setting).locals`
3. the `locals` hash / JSON object contains all the values needed for rendering a screen
4. files inside `/views` interpolate values from `locals` using ERB syntax (`<%= var %>`)
5. views prefixed with `_`, for example `_common`, are called "partials" (or 'components' in other frameworks)
6. shared code is not intended to "just work" but to showcase which values, and how, are extracted from 3rd party apps for TRMNL screen generation

## Plugin utilities

- [trmnl_preview](https://github.com/schrockwell/trmnl_preview) by [@schrockwell](https://github.com/schrockwell)
- [TRMNL plugin Dev Kit](https://github.com/sdjmchattie/trmnl-plugin-dev-kit) by [@sdjmchattie](https://github.com/sdjmchattie)
- [plugin generator [Laravel]](https://github.com/bnussbau/laravel-trmnl) by [@bnussbau](https://github.com/bnussbau)
- [TRMNL api simulator](https://github.com/deisterhold/trmnl-simulator) by [@deisterhold](https://github.com/deisterhold)
- [TRMNL Tips & Tricks](https://github.com/yunruse/trmnl-tricks) by [@yunruse](https://github.com/yunruse)

## Community plugins

- [(USA) Top 10 College Football Rankings](/lib/usa_college_football_rankings.md) by [@SnarfulSolutionsGroup](https://github.com/SnarfulSolutionsGroup) & [@Sitnik](https://github.com/Sitnik)
- [xkcd comics](https://github.com/SnarfulSolutionsGroup/TRMNL-Plugins/blob/main/TRMNL_Comic.md) by [@SnarfulSolutionsGroup](https://github.com/SnarfulSolutionsGroup)
- [Todoist](https://github.com/Nynir/trmnl-todoist) by [@Nynir](https://github.com/Nynir)
- [Surf reports](https://github.com/pcifaldi/surf_api) by [@pcifaldi](https://github.com/pcifaldi)
- [On This Day (in history)](https://github.com/frethop/TRMNL-thisday) by [@frethop](https://github.com/frethop)
- [Multi-column ICS calendar](https://github.com/jfsso/trmnl-calendar) by [@jfsso](https://github.com/jfsso)
- [WooCommerce](https://github.com/yannicschuller/trmnl-woocommerce) by [@yannicschuller](https://github.com/yannicschuller)
- [Strava goals](https://github.com/vinayak-mehta/trmnl-strava-goals) by [@vinayak-mehta](https://github.com/vinayak-mehta)
- [Valorant Tracker](https://github.com/MarkHopper24/Valorant-Tools) by [@MarkHopper24](https://github.com/MarkHopper24)
- [Marvel Rivals Stat Tracker](https://github.com/MarkHopper24/Marvel-Rivals-TRMNL-Tracker) by [@MarkHopper24](https://github.com/MarkHopper24)
- [NASA Deep Space Network](https://github.com/schrockwell/trmnl-dsn) by [@schrockwell](https://github.com/schrockwell)
- [Marvel Character of the Day](https://github.com/MarkHopper24/Marvel-Character-of-the-Day) by [@MarkHopper24](https://github.com/MarkHopper24)
- [Remember The Milk](https://github.com/sejtenik/trmnl-rtm-plugin) by [@sejtenik](https://github.com/sejtenik)
- [Habitify](https://github.com/sejtenik/trmnl-habitify-plugin) by [@sejtenik](https://github.com/sejtenik)
- [Libra](https://github.com/sejtenik/trmnl-libra-cloud-plugin) by [@sejtenik](https://github.com/sejtenik)
- [This Day in History (Wikipedia)](https://github.com/jvivona/TRMNL-recipes/tree/main/thisdayinhistory) by [@jvivona](https://github.com/jvivona)
- [Weekly Goal Tracker](https://github.com/azjgard/trmnl-weekly-goal-tracker) by [@azjgard](https://github.com/azjgard)
- [METAR](https://github.com/schrockwell/trmnl-metar) by [@schrockwell](https://github.com/schrockwell)
- [Block Clock](https://github.com/tyler-dot-earth/trmnl-notblockclock) by [@tyler-dot-earth](https://github.com/tyler-dot-earth)
- [TickTick Calendar](https://github.com/frethop/TRMNL-ticktick) by [@frethop](https://github.com/frethop)
- [Transport for London (TfL) status messages](https://github.com/stevekennedyuk/trmnl-tfl-status) by [@stevekennedyuk](https://github.com/stevekennedyuk)
- [Home Assistant - sensor data](https://github.com/gitstua/trmnl-plugin-dev/tree/main/home-assistant-trmnl#home-assistant-trmnl-plugin) by [@gitstua](https://github.com/gitstua)
- [Home Assistant - TRMNL data](https://github.com/Beat2er/homeassistant-trmnl-battery) by [@Beat2er](https://github.com/Beat2er)
- [Home Assistant - Weather Station](https://github.com/TilmanGriesel/ha_trmnl_weather_station) by [@TilmanGriesel](https://github.com/TilmanGriesel)
- [Bring! Shopping List](https://github.com/yshrdbrn/trmnl-bring-plugin) by [@yshrdbrn](https://github.com/yshrdbrn)
- [FLightBoard - airport activity](https://github.com/alexvarney/trmnl-flights) by [@alexvarney](https://github.com/alexvarney)
- [Netatmo + Tomorrow.io Weather API](https://github.com/simonjodet/weather_api?tab=readme-ov-file#trmnl-template-example) by [@simonjodet](https://github.com/simonjodet)
- [ÖBB (Austria) Train Monitor](https://github.com/bnussbau/trmnl-train-monitor) by [@bnussbau](https://github.com/bnussbau)
- [Buienradar](https://github.com/Akisame-AI/TRMNL_buienradar/) by [@Akisame-AI](https://github.com/Akisame-AI)
- [Random Steam Deals of the Day](https://github.com/subtype-space/trmnl-steam-deals) by [@asubowo / subtype](https://github.com/subtype-space)
- [Countdown plugin](https://github.com/jvdmeij/trmnl-countdown) by [@jvdmeij](https://github.com/jvdmei)
- [Crypto Fear & Greed](https://github.com/jvdmeij/trmnl-crypto-fear-and-greed) by [@jvdmeij](https://github.com/jvdmei)
- [Your Life in Weeks](https://github.com/jvdmeij/trmnl-your-life-in-weeks) by [@jvdmeij](https://github.com/jvdmei)
- [Magic 8-Ball](https://github.com/jvdmeij/trmnl-magic-8-ball) by [@jvdmeij](https://github.com/jvdmei)
- [Winnie the Pooh quote](https://github.com/jvdmeij/trmnl-winnie-the-pooh) by [@jvdmeij](https://github.com/jvdmei)
- [Word Clock](https://github.com/jvdmeij/trmnl-word-clock) by [@jvdmeij](https://github.com/jvdmei)
- [LastFM](https://github.com/monsieurm/trmnl-lastfm) by [@monsieurm](https://github.com/monsieurm)
- [Year In Progress](https://github.com/monsieurm/trmnl-yearinprogress) by [@monsieurm](https://github.com/monsieurm)
- [Who's That Pokémon?](https://github.com/sriniketh/trmnl-plugin-whos-that-pokemon) by [@sriniketh](https://github.com/sriniketh)
- [Canvas](https://github.com/JoshuaBrest/canvas-trmnl) by [@JoshuaBrest](https://github.com/JoshuaBrest)
- [Anime of the Day](https://github.com/Saious119/trmnl-anime-of-the-day/) by [@Saious119](https://github.com/Saious119)
- [BVG (Berlin) Public Transport](https://github.com/danmunoz/trmnl-bvg-transit) by [@Danmunoz](https://github.com/danmunoz)
- [Bluesky](https://github.com/solimaniac/trmnl-bsky) by [@solimaniac](https://github.com/solimaniac)
- [YoLink Temperature](https://github.com/erikbuild/trmnl-yolink-temperature) by [@erikbuild](https://github.com/erikbuild)

to be featured here, add `trmnl` topic to your repo, then open a PR or join the developer-only Discord server (link inside TRMNL UI).
