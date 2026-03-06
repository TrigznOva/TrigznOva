"""
Configuration module for the Pain Point Detector scraping pipeline.

Contains target subreddits organized by category, frustration keywords
for search queries, Trustpilot company slugs, and Product Hunt categories.
"""

# ---------------------------------------------------------------------------
# Reddit subreddits grouped by thematic category
# ---------------------------------------------------------------------------
SUBREDDITS: dict[str, list[str]] = {
    "business": [
        "smallbusiness",
        "entrepreneur",
        "startups",
        "SaaS",
        "indiehackers",
        "ecommerce",
        "dropship",
    ],
    "freelance": [
        "freelance",
        "Upwork",
        "fiverr",
        "webdev",
        "graphic_design",
        "copywriting",
    ],
    "tech": [
        "software",
        "sysadmin",
        "devops",
        "programming",
        "webdev",
        "learnprogramming",
        "cscareerquestions",
    ],
    "consumer": [
        "mildlyinfuriating",
        "firstworldproblems",
        "CrappyDesign",
        "assholedesign",
        "softwaregore",
    ],
    "specific_industries": [
        "teachers",
        "nursing",
        "accounting",
        "realestate",
        "fitness",
        "restaurants",
        "legaladvice",
    ],
    "general": [
        "AskReddit",
        "LifeProTips",
        "DoesAnybodyElse",
        "NoStupidQuestions",
        "TrueOffMyChest",
    ],
}

# ---------------------------------------------------------------------------
# Keywords that signal frustration, pain, or unmet needs
# ---------------------------------------------------------------------------
PAIN_KEYWORDS: list[str] = [
    "frustrated",
    "frustrating",
    "annoying",
    "annoyed",
    "hate",
    "terrible",
    "awful",
    "worst",
    "broken",
    "waste of time",
    "waste of money",
    "scam",
    "rip off",
    "overpriced",
    "unusable",
    "buggy",
    "unreliable",
    "disappointing",
    "nightmare",
    "horrible",
    "painful",
    "struggle",
    "struggling",
    "impossible",
    "can't stand",
    "fed up",
    "sick of",
    "tired of",
    "wish there was",
    "why is it so hard",
    "there has to be a better way",
    "looking for alternative",
]

# ---------------------------------------------------------------------------
# Trustpilot company slugs (SaaS, services, telecom, banking)
# ---------------------------------------------------------------------------
TRUSTPILOT_COMPANIES: list[str] = [
    # Animals Pets (8 companies)
    "rover.com",  # Rover.com | Pet Sitting — 31383 reviews
    "westandwillow.com",  # West & Willow — 19331 reviews
    "paw-champ.com",  # PawChamp — 16418 reviews
    "spotpet.com",  # Spot Pet Insurance — 10349 reviews
    "pawrade.com",  # Pawrade — 6783 reviews
    "dutch.com",  # Dutch — 3536 reviews
    "muddymats.com",  # Muddy Mat® — 2517 reviews
    "birdfy.com",  # Birdfy — 694 reviews
    # Beauty Wellbeing (10 companies)
    "www.fashionnova.com",  # Fashion Nova — 182945 reviews
    "ilmakiage.com",  # IL MAKIAGE New York — 90100 reviews
    "simple-life-app.com",  # Simple Life App — 36908 reviews
    "ivimhealth.com",  # Ivím Health — 35028 reviews
    "giftexpress.com",  # GiftExpress — 21134 reviews
    "orthofeet.com",  # Orthofeet — 18686 reviews
    "joinmochi.com",  # Mochi Health — 15115 reviews
    "spoiledchild.com",  # SpoiledChild — 5516 reviews
    "joinamble.com",  # Amble Health — 3079 reviews
    "welzo.com",  # welmarto — 2371 reviews
    # Business Services (10 companies)
    "www.toluna.com",  # Toluna — 212403 reviews
    "derila.com",  # Derila Pillow — 36053 reviews
    "www.zazzle.com",  # Zazzle  — 28340 reviews
    "stickerapp.com",  # StickerApp Inc. — 18007 reviews
    "deel.com",  # Deel — 8509 reviews
    "vitalformsdirect.com",  # Vitalformsdirect — 7071 reviews
    "supportnerds.us",  # Support Nerds Inc. — 6519 reviews
    "cyclopure.com",  # Cyclopure — 491 reviews
    "marketerhire.com",  # MarketerHire — 320 reviews
    "hubbed.com.au",  # PARCELPOINT — 220 reviews
    # Construction Manufactoring (8 companies)
    "outsidepride.com",  # Outsidepride.com, Inc. — 3883 reviews
    "www.fridayparts.com",  # FridayParts — 1832 reviews
    "bullionexchanges.com",  # Bullion Exchanges — 1053 reviews
    "eyemartexpress.com",  # Eyemart Express — 953 reviews
    "enphase.com",  # Enphase Energy — 464 reviews
    "us.openinfra.com",  # Open Infra US — 377 reviews
    "www.jmac.com",  # JMAC Supply — 261 reviews
    "orosresearch.com",  # OROS Research — 148 reviews
    # Education Training (10 companies)
    "myiq.com",  # MyIQ — 103715 reviews
    "www.myheritage.com",  # MyHeritage — 87452 reviews
    "preply.com",  # Preply  — 20445 reviews
    "www.monster.com",  # Monster - Job Search & Resume Builder — 19381 reviews
    "riseguide.com",  # Riseguide — 12320 reviews
    "aceableagent.com",  # AceableAgent — 10829 reviews
    "skyfluence-beauty.com",  # Skyfluence Beauty — 4818 reviews
    "www.alignerr.com",  # Alignerr — 1606 reviews
    "contractortrainingcenter.com",  # Contractor Training Center — 333 reviews
    "contrarianthinking.co",  # Contrarian Thinking  — 308 reviews
    # Electronics Technology (9 companies)
    "www.otterbox.com",  # OtterBox — 85524 reviews
    "www.norton.com",  # Norton — 65786 reviews
    "transak.com",  # Transak — 48243 reviews
    "files-editor.com",  # Files Editor — 34361 reviews
    "ecoatm.com",  # ecoATM — 22446 reviews
    "vinclarity.com",  # vinclarity.com — 16402 reviews
    "phobio.com",  # Phobio — 8928 reviews
    "www.dwp.gov.uk",  # DWP — 1391 reviews
    "ezvizlife.com",  # EZVIZ — 527 reviews
    # Events Entertainment (10 companies)
    "www.crowncoinscasino.com",  # CrownCoins Casino — 171945 reviews
    "iggm.com",  # IGGM — 163528 reviews
    "surveys.gobranded.com",  # Branded Surveys — 117226 reviews
    "www.gunbroker.com",  # GunBroker.com — 50919 reviews
    "asknebula.com",  # Nebula — 30360 reviews
    "zulacasino.com",  # Zula Casino — 28270 reviews
    "gamenerdz.com",  # Game Nerdz — 15589 reviews
    "hint.app",  # hint.app — 10467 reviews
    "missacc.com",  # Missacc — 6833 reviews
    "www.ftd.com",  # FTD — 2610 reviews
    # Food Beverages Tobacco (10 companies)
    "factor75.com",  # Factor_ — 91189 reviews
    "hellofresh.com",  # HelloFresh US — 82441 reviews
    "azurestandard.com",  # Azure Standard — 71440 reviews
    "goodranchers.com",  # Good Ranchers — 25413 reviews
    "ecigmafia.com",  # ECigMafia — 21413 reviews
    "vivino.com",  # Vivino — 19174 reviews
    "ryzesuperfoods.com",  # RYZE Superfoods — 11013 reviews
    "drdabber.com",  # Dr. Dabber  — 9586 reviews
    "www.hungryroot.com",  # Hungryroot — 6827 reviews
    "ohnuts.com",  # Oh! Nuts — 3927 reviews
    # Health Medical (9 companies)
    "www.glassesusa.com",  # GlassesUSA — 122680 reviews
    "honehealth.com",  # Hone Health — 10363 reviews
    "wisey.app",  # Wisey — 5114 reviews
    "tryeden.com",  # Eden — 2856 reviews
    "stantonoptical.com",  # Stanton Optical — 1866 reviews
    "nurx.com",  # Nurx — 1499 reviews
    "emotionalsupportanimal.com",  # Emotionalsupportanimal — 640 reviews
    "doctoralexa.com",  # Doctor Alexa — 564 reviews
    "buyhearingaid.com",  # Buyhearingaid — 100 reviews
    # Hobbies Crafts (6 companies)
    "www.thriftbooks.com",  # ThriftBooks — 2670805 reviews
    "stockx.com",  # StockX — 241070 reviews
    "www.jwpepper.com",  # J.W. Pepper — 20545 reviews
    "www.alibris.com",  # Alibris — 19958 reviews
    "yeti.com",  # YETI — 16688 reviews
    "brambleberry.com",  # Bramble Berry — 3722 reviews
    # Home Garden (6 companies)
    "www.wolfandbadger.com",  # Wolf & Badger — 57171 reviews
    "taskrabbit.com",  # Taskrabbit North America — 53165 reviews
    "www.ikea.com",  # IKEA — 28733 reviews
    "avasflowers.net",  # AvasFlowers — 18618 reviews
    "lulutox.com",  # Lulutox — 9263 reviews
    "www.blossomflowerdelivery.com",  # Blossomflowerdelivery — 8874 reviews
    # Home Services (8 companies)
    "www.selfstorage.com",  # SelfStorage.com — 76996 reviews
    "vivint.com",  # Vivint — 58601 reviews
    "aptivepestcontrol.com",  # Aptive Pest Control — 27644 reviews
    "ahs.com",  # American Home Shield — 14696 reviews
    "www.collegehunkshaulingjunk.com",  # College HUNKS Hauling Junk and Moving — 6789 reviews
    "lockly.com",  # Lockly — 567 reviews
    "50floor.com",  # 50 Floor — 555 reviews
    "caddymoving.com",  # Caddy Moving — 481 reviews
    # Legal Services Government (9 companies)
    "cordobalegal.com",  # Cordoba Legal Group — 48838 reviews
    "www.incauthority.com",  # Inc Authority — 45755 reviews
    "www.legalzoom.com",  # LegalZoom — 28250 reviews
    "www.zenbusiness.com",  # ZenBusiness — 27291 reviews
    "bizee.com",  # Bizee — 24406 reviews
    "tailorbrands.com",  # Tailor Brands — 12023 reviews
    "www.askalawyeroncall.com",  # Askalawyeroncall — 10888 reviews
    "www.legalnature.com",  # LegalNature — 9798 reviews
    "trackmyvisanow.com",  # Track My Visa Now — 516 reviews
    # Media Publishing (5 companies)
    "www.mediamarkt.nl",  # MediaMarkt NL — 62927 reviews
    "bookshop.org",  # Bookshop.org — 49897 reviews
    "instaheadshots.com",  # InstaHeadshots — 9185 reviews
    "foreversongs.com",  # ForeverSongs — 1988 reviews
    "tellmytale.com",  # Tellmytale — 1821 reviews
    # Money Insurance (10 companies)
    "www.allianztravelinsurance.com",  # Allianz Partners USA — 171605 reviews
    "thegeneral.com",  # The General® — 132056 reviews
    "www.quicken.com",  # Quicken — 72258 reviews
    "simplex.com",  # Simplex — 28679 reviews
    "reprisefinancial.com",  # Reprise Financial — 21493 reviews
    "exeterfinance.com",  # Exeter Finance — 13941 reviews
    "mysympleloan.com",  # My Symple Loan — 6317 reviews
    "lili.co",  # Lili — 4062 reviews
    "mynd.co",  # Mynd Management — 1943 reviews
    "sunrisebusinesscapital.com",  # Sunrise Business Capital — 136 reviews
    # Public Local Services (5 companies)
    "www.justanswer.com",  # JustAnswer — 126249 reviews
    "askanexpertonline.com",  # Askanexpertonline.com — 4738 reviews
    "goodcar.com",  # GoodCar — 4309 reviews
    "askadoctor.help",  # Askadoctor — 3756 reviews
    "lexialearning.com",  # Lexia Learning — 272 reviews
    # Restaurants Bars (7 companies)
    "flexpromeals.com",  # FlexPro Meals — 11958 reviews
    "fultonfishmarket.com",  # Fulton Fish Market — 11184 reviews
    "www.justeat.co.uk",  # Just Eat UK — 6414 reviews
    "www.yelp.com",  # Yelp — 5946 reviews
    "webstaurantstore.com",  # WebstaurantStore — 3248 reviews
    "www.mcdonalds.com",  # McDonald's — 2347 reviews
    "marriottvacationclub.com",  # Marriott Vacation Club — 435 reviews
    # Shopping Fashion (7 companies)
    "www.teepublic.com",  # TeePublic — 584544 reviews
    "thehalara.com",  # Halara — 376919 reviews
    "therealreal.com",  # The RealReal — 122696 reviews
    "www.govets.com",  # GoVets — 6623 reviews
    "www.brilliance.com",  # Brilliance.com — 4457 reviews
    "familypanda.co",  # Family Panda — 594 reviews
    "www.nobalifestyle.com",  # Nobalifestyle — 243 reviews
    # Sports (8 companies)
    "shapellx.com",  # Shapellx — 45868 reviews
    "sidelineswap.com",  # SidelineSwap — 13479 reviews
    "www.holabirdsports.com",  # Holabird Sports — 10185 reviews
    "canyoncoolers.com",  # Canyon Coolers — 5482 reviews
    "us.speedo.com",  # us.speedo.com — 4367 reviews
    "powermetercity.com",  # Power Meter City — 3926 reviews
    "www.movesmethod.com",  # Movesmethod — 2164 reviews
    "hollowsocks.com",  # Hollow Socks — 1099 reviews
    # Travel Vacation (8 companies)
    "www.viator.com",  # Viator.com — 305901 reviews
    "www.gotogate.com",  # Gotogate — 147923 reviews
    "www.asaptickets.com",  # ASAP Tickets — 105600 reviews
    "guestreservations.com",  # Guest Reservations — 54540 reviews
    "www.cheapoair.com",  # CheapOair.com — 33321 reviews
    "reserve2.hotelguides.com",  # Reserve2 Hotelguides — 2867 reviews
    "ymtvacations.com",  # YMT Vacations — 2455 reviews
    "floridarentals.com",  # FloridaRentals — 530 reviews
    # Utilities (5 companies)
    "igs.com",  # IGS Energy — 27456 reviews
    "electricityrates.com",  # electricityrates.com — 6999 reviews
    "renogy.com",  # Renogy — 6923 reviews
    "www.eco-worthy.com",  # ECO-WORTHY — 1352 reviews
    "www.northernpowergrid.com",  # Northern Powergrid — 216 reviews
    # Vehicles Transportation (8 companies)
    "peddle.com",  # Peddle — 183867 reviews
    "www.getaround.com",  # Getaround — 87416 reviews
    "turo.com",  # Turo — 78815 reviews
    "www.servicingstop.co.uk",  # Servicing Stop — 73647 reviews
    "intoxalock.com",  # Intoxalock — 71044 reviews
    "tireagent.com",  # Tire Agent — 8195 reviews
    "seatbeltextenderpros.com",  # Seat Belt Extender Pros — 6236 reviews
    "oxcarcare.com",  # Ox Car Care, Inc.  — 209 reviews
]

# ---------------------------------------------------------------------------
# Product Hunt categories to monitor
# ---------------------------------------------------------------------------
PRODUCTHUNT_CATEGORIES: list[str] = [
    "developer-tools",
    "productivity",
    "saas",
    "marketing",
    "design-tools",
    "artificial-intelligence",
    "fintech",
    "health-fitness",
    "education",
    "e-commerce",
    "communication",
    "analytics",
    "no-code",
    "remote-work",
    "customer-support",
]

# ---------------------------------------------------------------------------
# Hacker News scraping parameters
# ---------------------------------------------------------------------------
HACKERNEWS_SEARCH_MONTHS: int = 12
HACKERNEWS_TYPES: list[str] = ["story", "comment"]

# ---------------------------------------------------------------------------
# Stack Overflow scraping parameters
# ---------------------------------------------------------------------------
STACKOVERFLOW_SEARCH_MONTHS: int = 12
# Sites to search (could add "serverfault", "superuser" later)
STACKOVERFLOW_SITES: list[str] = ["stackoverflow"]

# ---------------------------------------------------------------------------
# Dev.to scraping parameters
# ---------------------------------------------------------------------------
# Tags likely to contain frustrated / opinionated content
DEVTO_TAGS: list[str] = [
    "discuss",
    "help",
    "watercooler",
    "webdev",
    "programming",
    "career",
    "productivity",
    "testing",
    "devops",
    "beginners",
]

# ---------------------------------------------------------------------------
# Bluesky scraping parameters
# ---------------------------------------------------------------------------
BLUESKY_SEARCH_MONTHS: int = 6  # Bluesky is newer, less historical content

# ---------------------------------------------------------------------------
# Lemmy scraping parameters
# ---------------------------------------------------------------------------
LEMMY_INSTANCES: list[str] = [
    "https://lemmy.world",
    "https://lemmy.ml",
    "https://programming.dev",
    "https://lemm.ee",
    "https://sh.itjust.works",
]
