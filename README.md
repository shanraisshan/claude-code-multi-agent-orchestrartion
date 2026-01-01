# Claude Code Multi-Agent Orchestration

Run `/orchestrate` in Claude Code CLI to fetch temperatures from **195 countries** in parallel, then calculate their average.

```
/orchestrate
```

```
                    ┌─────────────────────────────┐
                    │        /orchestrate         │
                    └──────────────┬──────────────┘
                                   │
    ┌──────────────────────────────┼──────────────────────────────┐
    │              │               │               │              │
    ▼              ▼               ▼               ▼              ▼
┌────────┐   ┌────────┐   ┌ ─ ─ ─ ─ ─ ─   ┌────────┐   ┌────────┐
│Afghan- │   │Albania │      195 Weather  │Zimbabwe│   │ Zambia │
│istan   │   │ Agent  │   │    Agents    ││ Agent  │   │ Agent  │
│ Agent  │   │(yellow)│    (in parallel)  │(yellow)│   │(yellow)│
│(yellow)│   └───┬────┘   └ ─ ─ ─ ┬ ─ ─ ┘ └───┬────┘   └───┬────┘
└───┬────┘       │               │            │            │
    │            │               │            │            │
    └────────────┴───────────────┼────────────┴────────────┘
                                 │
                                 ▼
                   ┌─────────────────────────────┐
                   │    Weather Writer Agent     │
                   │            (red)            │
                   └──────────────┬──────────────┘
                                  │
                                  ▼
                   ┌─────────────────────────────┐
                   │   Weather Average Agent     │
                   │           (green)           │
                   └─────────────────────────────┘
```

## Agent Summary

| Agent Type | Count | Color | Description |
|------------|-------|-------|-------------|
| Weather Country Agents | 195 | 🟡 Yellow | Fetch temperature for each country's capital |
| Weather Writer Agent | 1 | 🔴 Red | Writes temperatures to `output/temperatures.md` |
| Weather Average Agent | 1 | 🟢 Green | Calculates average and writes to `output/average.md` |

## All 195 Countries

<details>
<summary>Click to expand full country list</summary>

| # | Country | Capital |
|---|---------|---------|
| 1 | Afghanistan | Kabul |
| 2 | Albania | Tirana |
| 3 | Algeria | Algiers |
| 4 | Andorra | Andorra la Vella |
| 5 | Angola | Luanda |
| 6 | Antigua and Barbuda | Saint John's |
| 7 | Argentina | Buenos Aires |
| 8 | Armenia | Yerevan |
| 9 | Australia | Canberra |
| 10 | Austria | Vienna |
| 11 | Azerbaijan | Baku |
| 12 | Bahamas | Nassau |
| 13 | Bahrain | Manama |
| 14 | Bangladesh | Dhaka |
| 15 | Barbados | Bridgetown |
| 16 | Belarus | Minsk |
| 17 | Belgium | Brussels |
| 18 | Belize | Belmopan |
| 19 | Benin | Porto-Novo |
| 20 | Bhutan | Thimphu |
| 21 | Bolivia | La Paz |
| 22 | Bosnia and Herzegovina | Sarajevo |
| 23 | Botswana | Gaborone |
| 24 | Brazil | Brasília |
| 25 | Brunei | Bandar Seri Begawan |
| 26 | Bulgaria | Sofia |
| 27 | Burkina Faso | Ouagadougou |
| 28 | Burundi | Gitega |
| 29 | Cabo Verde | Praia |
| 30 | Cambodia | Phnom Penh |
| 31 | Cameroon | Yaoundé |
| 32 | Canada | Ottawa |
| 33 | Central African Republic | Bangui |
| 34 | Chad | N'Djamena |
| 35 | Chile | Santiago |
| 36 | China | Beijing |
| 37 | Colombia | Bogotá |
| 38 | Comoros | Moroni |
| 39 | Congo (DRC) | Kinshasa |
| 40 | Congo (Republic) | Brazzaville |
| 41 | Costa Rica | San José |
| 42 | Côte d'Ivoire | Yamoussoukro |
| 43 | Croatia | Zagreb |
| 44 | Cuba | Havana |
| 45 | Cyprus | Nicosia |
| 46 | Czechia | Prague |
| 47 | Denmark | Copenhagen |
| 48 | Djibouti | Djibouti |
| 49 | Dominica | Roseau |
| 50 | Dominican Republic | Santo Domingo |
| 51 | Ecuador | Quito |
| 52 | Egypt | Cairo |
| 53 | El Salvador | San Salvador |
| 54 | Equatorial Guinea | Malabo |
| 55 | Eritrea | Asmara |
| 56 | Estonia | Tallinn |
| 57 | Eswatini | Mbabane |
| 58 | Ethiopia | Addis Ababa |
| 59 | Fiji | Suva |
| 60 | Finland | Helsinki |
| 61 | France | Paris |
| 62 | Gabon | Libreville |
| 63 | Gambia | Banjul |
| 64 | Georgia | Tbilisi |
| 65 | Germany | Berlin |
| 66 | Ghana | Accra |
| 67 | Greece | Athens |
| 68 | Grenada | Saint George's |
| 69 | Guatemala | Guatemala City |
| 70 | Guinea | Conakry |
| 71 | Guinea-Bissau | Bissau |
| 72 | Guyana | Georgetown |
| 73 | Haiti | Port-au-Prince |
| 74 | Honduras | Tegucigalpa |
| 75 | Hungary | Budapest |
| 76 | Iceland | Reykjavik |
| 77 | India | New Delhi |
| 78 | Indonesia | Jakarta |
| 79 | Iran | Tehran |
| 80 | Iraq | Baghdad |
| 81 | Ireland | Dublin |
| 82 | Israel | Jerusalem |
| 83 | Italy | Rome |
| 84 | Jamaica | Kingston |
| 85 | Japan | Tokyo |
| 86 | Jordan | Amman |
| 87 | Kazakhstan | Astana |
| 88 | Kenya | Nairobi |
| 89 | Kiribati | Tarawa |
| 90 | Kuwait | Kuwait City |
| 91 | Kyrgyzstan | Bishkek |
| 92 | Laos | Vientiane |
| 93 | Latvia | Riga |
| 94 | Lebanon | Beirut |
| 95 | Lesotho | Maseru |
| 96 | Liberia | Monrovia |
| 97 | Libya | Tripoli |
| 98 | Liechtenstein | Vaduz |
| 99 | Lithuania | Vilnius |
| 100 | Luxembourg | Luxembourg City |
| 101 | Madagascar | Antananarivo |
| 102 | Malawi | Lilongwe |
| 103 | Malaysia | Kuala Lumpur |
| 104 | Maldives | Malé |
| 105 | Mali | Bamako |
| 106 | Malta | Valletta |
| 107 | Marshall Islands | Majuro |
| 108 | Mauritania | Nouakchott |
| 109 | Mauritius | Port Louis |
| 110 | Mexico | Mexico City |
| 111 | Micronesia | Palikir |
| 112 | Moldova | Chișinău |
| 113 | Monaco | Monaco |
| 114 | Mongolia | Ulaanbaatar |
| 115 | Montenegro | Podgorica |
| 116 | Morocco | Rabat |
| 117 | Mozambique | Maputo |
| 118 | Myanmar | Naypyidaw |
| 119 | Namibia | Windhoek |
| 120 | Nauru | Yaren |
| 121 | Nepal | Kathmandu |
| 122 | Netherlands | Amsterdam |
| 123 | New Zealand | Wellington |
| 124 | Nicaragua | Managua |
| 125 | Niger | Niamey |
| 126 | Nigeria | Abuja |
| 127 | North Korea | Pyongyang |
| 128 | North Macedonia | Skopje |
| 129 | Norway | Oslo |
| 130 | Oman | Muscat |
| 131 | Pakistan | Islamabad |
| 132 | Palau | Ngerulmud |
| 133 | Palestine | Ramallah |
| 134 | Panama | Panama City |
| 135 | Papua New Guinea | Port Moresby |
| 136 | Paraguay | Asunción |
| 137 | Peru | Lima |
| 138 | Philippines | Manila |
| 139 | Poland | Warsaw |
| 140 | Portugal | Lisbon |
| 141 | Qatar | Doha |
| 142 | Romania | Bucharest |
| 143 | Russia | Moscow |
| 144 | Rwanda | Kigali |
| 145 | Saint Kitts and Nevis | Basseterre |
| 146 | Saint Lucia | Castries |
| 147 | Saint Vincent and the Grenadines | Kingstown |
| 148 | Samoa | Apia |
| 149 | San Marino | San Marino |
| 150 | São Tomé and Príncipe | São Tomé |
| 151 | Saudi Arabia | Riyadh |
| 152 | Senegal | Dakar |
| 153 | Serbia | Belgrade |
| 154 | Seychelles | Victoria |
| 155 | Sierra Leone | Freetown |
| 156 | Singapore | Singapore |
| 157 | Slovakia | Bratislava |
| 158 | Slovenia | Ljubljana |
| 159 | Solomon Islands | Honiara |
| 160 | Somalia | Mogadishu |
| 161 | South Africa | Pretoria |
| 162 | South Korea | Seoul |
| 163 | South Sudan | Juba |
| 164 | Spain | Madrid |
| 165 | Sri Lanka | Colombo |
| 166 | Sudan | Khartoum |
| 167 | Suriname | Paramaribo |
| 168 | Sweden | Stockholm |
| 169 | Switzerland | Bern |
| 170 | Syria | Damascus |
| 171 | Tajikistan | Dushanbe |
| 172 | Tanzania | Dodoma |
| 173 | Thailand | Bangkok |
| 174 | Timor-Leste | Dili |
| 175 | Togo | Lomé |
| 176 | Tonga | Nuku'alofa |
| 177 | Trinidad and Tobago | Port of Spain |
| 178 | Tunisia | Tunis |
| 179 | Turkey | Ankara |
| 180 | Turkmenistan | Ashgabat |
| 181 | Tuvalu | Funafuti |
| 182 | Uganda | Kampala |
| 183 | Ukraine | Kyiv |
| 184 | United Arab Emirates | Abu Dhabi |
| 185 | United Kingdom | London |
| 186 | United States | Washington D.C. |
| 187 | Uruguay | Montevideo |
| 188 | Uzbekistan | Tashkent |
| 189 | Vanuatu | Port Vila |
| 190 | Vatican City | Vatican City |
| 191 | Venezuela | Caracas |
| 192 | Vietnam | Hanoi |
| 193 | Yemen | Sana'a |
| 194 | Zambia | Lusaka |
| 195 | Zimbabwe | Harare |

</details>

## Output Files

- `output/temperatures.md` - Contains temperatures for all 195 countries
- `output/average.md` - Contains the calculated global average temperature
