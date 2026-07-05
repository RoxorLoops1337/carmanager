# CarManager: The Game (Design Plan)

A cozy but shady car dealing simulation set in 1990s Belgium. You run CarManager, a small used car business. Buy cars cheap in the East, drive them home on ZZ transit plates, "prepare" them in the garage, and sell them to Belgian customers. Get rich without getting caught.

## Platform

Single HTML file, runs in any browser on PC and mobile (responsive, touch friendly). Saves automatically in the browser (localStorage) plus manual export/import save codes. Can later be wrapped as an Android APK with no changes if wanted.

The 3D showroom uses Three.js with procedurally built low-poly cars (body shape per type, real paint colors). This keeps the game tiny and fast on phones. Downloading real 3D models from the web was considered but rejected for v1: files are 5-50 MB each, licensing is messy, and quality is inconsistent. The low-poly look fits the cute/cozy style. Real downloaded models can be added later for a "collector edition".

## Setting

- Year: 1995, week-based time. Currency: Belgian Francs (BEF).
- HQ: a small lot in Essene, right next to bus stop Koudenberg. Ambitious owners can later upgrade to a proper showroom in Zellik (more walk-in customers, better prices, higher rent).
- The office runs on cigarettes and Red Bull. Smoke breaks on the koertje calm the nerves (a little less heat), a fresh Red Bull sharpens your next negotiation.
- The business looks legit from the street. Behind the garage door, less so.

## The Three Characters

**Martine (The CEO).** Makes everything happen. Perks: starts with more capital and a bank credit line, official paperwork is cheaper and faster (ZZ plates at a discount), customers pay a bit more because the shop looks respectable. Weakness: shady services (odometer man, paper man) cost extra because her contacts are "clean".

**Alin (The Fixer).** Knows a guy for everything, especially in Katowice. Perks: buys cheaper abroad, finds rare "no questions asked" cars, odometer rollbacks and dodgy papers cost half, bribes work better. Weakness: he skims from the till. Every week a little money quietly disappears. Also starts with some heat on him already.

**Thomas (The Charmer).** The good guy, more or less. Perks: best haggler on both sides, reputation grows faster, angry customers forgive him, sells at premium prices. Weakness: less starting cash, and his conscience means shady actions raise heat faster for him (he is bad at lying to inspectors).

## Core Loop

1. **Buy trip.** Pick a destination: Germany (clean expensive cars), Netherlands (fair deals), Poland (cheap, risky, some hot cars), Ukraine (dirt cheap, rare finds, wild risks). Travel costs money and a week. Each market shows 4-6 randomly generated cars: real model, year, km, condition, paint, papers quality, asking price. Haggle.
2. **Drive it home.** Oregon-Trail style journey with random events: customs checks, police controls, breakdowns, snow, hitchhikers, bribe opportunities, rival dealers. Driving without a valid ZZ transit plate is possible but risky and expensive when caught.
3. **The garage.** Repair engine and body, respray, tune. Or the shady menu: roll back the odometer, freshen up the papers, hide accident damage with polish and silence.
4. **Sell.** Customers walk in weekly with wishes (cheap first car, family wagon, sporty coupe, collector piece, "something German"). Set your price, haggle, decide what to disclose. Selling a wreck as a pearl pays great until it comes back on a tow truck with an angry owner.
5. **Stay out of trouble.** Every shady act raises Heat. High heat triggers inspections: fines, confiscated cars with fake papers, court. Lay low or pay the right people. Reputation drives customer quality and volume.

## Key Systems

- **Cars: ~65 real models.** Mostly 90s (Golf III GTI, BMW E36, Mercedes W124, Opel Calibra, Peugeot 205 GTI, Lancia Delta Integrale, Supra MK4, RX-7...), some 80s (E30, 205, Manta), rarer 70s/60s/50s finds (2CV, DS, E-Type, Beetle, 300SL) that appear mostly in Ukraine barns. Rarity tiers: common, uncommon, rare, legend.
- **Car attributes:** year, km, engine condition, body condition, paint color, tuning level, quirks (ex-taxi, flood car, accident history, smells of cigarettes, "one careful owner"), papers (clean, dubious, fake).
- **ZZ plates:** needed to legally drive unregistered cars across borders. Official route: slow, needs reputation. Shady route: fast, pricey, and the plate might be... borrowed.
- **Heat and Reputation:** two dials that shape every decision.
- **Economy:** start ~750,000 BEF (Martine 1,000,000). Weekly costs: rent, coffee, Alin's fingers in the till. Win condition: none, it is a sandbox, but milestones celebrate your first million, first legend car, and surviving a full year.
- **3D Showroom:** any owned car can be admired on a rotating turntable in its actual color.

## Later Ideas (v2)

Staff hiring, rival dealer AI, auctions in Liège, character story missions, radio with fake 90s Belgian ads, downloaded high-detail 3D models.
