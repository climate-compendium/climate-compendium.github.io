---
author: sklimmer
layout: post
title:  "Carbon Brief"
date:   2019-10-18
categories: knowledge
sources:
- reg: CAN
  src: 
    - lng: en
      url: https://www.carbonbrief.org/the-carbon-brief-profile-canada
      pic: https://public.tableau.com/views/ClimatechangeprofileCanada/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&:origin=viz_share_link
- reg: IDN
  src:
    - lng: id
      url: https://www.carbonbrief.org/profil-carbon-brief-indonesia
      pic: https://public.tableau.com/views/ProfilCarbonBriefIndonesia/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&publish=yes&:origin=viz_share_link
    - lng: en
      url: https://www.carbonbrief.org/the-carbon-brief-profile-indonesia
      pic: https://public.tableau.com/views/ClimatechangeprofileIndonesia/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&:origin=viz_share_link
- reg: IND
  src: 
    - lng: en
      url: https://www.carbonbrief.org/the-carbon-brief-profile-india
      pic: https://www.carbonbrief.org/the-carbon-brief-profile-india
    - lng: in
      url: https://www.carbonbrief.org/the-carbon-brief-profile-bharat
      pic: https://public.tableau.com/views/1296/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&:origin=viz_share_link
- reg: ZAF
  src:
    - lng: en
      url: https://www.carbonbrief.org/the-carbon-brief-profile-south-africa
      pic: https://public.tableau.com/views/ClimatechangeprofileSouthAfrica/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&:origin=viz_share_link
- reg: JPN
  src:
    - lng: en
      url: https://www.carbonbrief.org/carbon-brief-profile-japan
      pic: https://public.tableau.com/views/ClimatechangeprofileJapan/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&publish=yes&:origin=viz_share_link
- reg: TUR
  src:
    - lng: en
      url: https://www.carbonbrief.org/carbon-brief-profile-turkey
      pic: https://public.tableau.com/views/ClimatechangeprofileTurkey/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&:origin=viz_share_link
    - lng: tr
      url: https://www.carbonbrief.org/carbon-brief-turkiye-profili
      pic: https://public.tableau.com/views/IklimdeiikliiprofiliTrkiye/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&publish=yes&:origin=viz_share_link
- reg: BRA
  src:
    - lng: en
      url: https://www.carbonbrief.org/the-carbon-brief-profile-brazil
      pic: https://public.tableau.com/views/ClimatechangeprofileBrazil/Dashboard1?:embed=y&:embed_code_version=3&:loadOrderID=0&:display_count=yes&publish=yes&:origin=viz_share_link
---
[Carbon Brief](https://www.carbonbrief.org) is a UK-based website covering the latest developments in climate science, climate policy and energy policy. They provide [profiles for several countries](https://www.carbonbrief.org/category/in-focus/country-profiles), which go beyond the data provide by [Our World in Data](https://ourworldindata.org/co2-and-other-greenhouse-gas-emissions) as they include more aspects, e.g. land use.

## Country profiles

{% assign sources = page.sources | sort: "reg" %}
{% for item in sources %}
   {% assign country = site.data.unsd | where:"iso3",item.reg | push:item.reg | first %}
- {{ country.c_o_a }}
    {% for src in item.src %}
    - [Carbon Brief ({{ src.lng }})]({{ src.url }})
    {% endfor %}
    <br/>
{% endfor %}

