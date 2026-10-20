# Trikon Bingo — Vercel par deploy kaise karein

Is folder me sirf ek file hai: `index.html` — yahi pura game hai (teeno modes: Player vs Computers, Pass & Play, Play Online).
Online multiplayer is file ke andar pehle se jude hue Firebase database (tumhara apna "trikon-bingo" project) se chalta hai — Vercel par kuch alag se setup nahi karna.

## Deploy ke steps (pehli baar, ~5 minute)

1. **Account banao:** [vercel.com](https://vercel.com) kholo → "Sign Up" → Google ya GitHub se login karo. Bilkul free plan (Hobby) milega, card nahi chahiye.
2. **Drop wala page kholo:** [vercel.com/drop](https://vercel.com/drop) — yahi Vercel ka official drag-and-drop deploy page hai (na Git chahiye, na koi software/terminal).
3. **File gira do:** Is folder ko **drag-and-drop** kar do — ya packet wali zip ko seedha gira do (nayi zip me `index.html` sabse upar hai, taaki root page apne aap mil jaye). Sirf `index.html` file akeli girana bhi chalega.
   - Team me apna personal account chuno, project ka naam `trikon-bingo` rakh do — link aisa milega: `trikon-bingo.vercel.app`
   - Framework wali setting me kuch mat chhedo — file jaisi hai waisi hi deploy hogi (seedhi static file hai, koi build nahi).
4. **Deploy dabao:** Vercel project bana kar seedha production par live kar dega — ~30 second me jo link mile, wahi doston ke liye hai.

## Jo verify karna hai deploy ke baad

- Link khol kar game aata hai ya nahi (title: Trikon Bingo).
- **Room wala link:** Play Online → room banao → jo invite link game de, use dusre phone/browser me kholo → room code apne aap bhara hona chahiye aur join ho jana chahiye. (Yahi wo cheez hai jo Muse wale link par redirect ki wajah se nahi hoti thi — Vercel ka pata seedha hai, isliye yahan honi chahiye.)
- Ek chhota game dono phones par khel kar number sync dekh lena.

## Aage updates kaise jayenge

- Jab bhi game me koi badlav hoga, main tumhe nayi `index.html` file dunga. Update ka pakka tareeka (Vercel docs ke hisaab se): Vercel dashboard me apne project par nayi file/folder **drop kar do** — usi project ka naya production deployment ban jayega, link wahi rahega. Sirf "Redeploy" dabane se purani file hi dobara chalegi, nayi nahi. (GitHub jod dein to har update apne aap live ho jayega — chaaho to wo setup bhi kar dunga.)
- Doston ko hamesha **Vercel wala link** bhejna. Muse wala purana link ek alag copy hai — us par updates nahi jayenge.

## Do zaroori baatein

- **Firebase rules ki miyad (18 November 2026)** hosting se alag hai — uski taiyaari jaari hai, samay par tumhe dikha kar pakke rules lagayenge.
- File ke andar Firebase ki web config hai — ye koi chhupa password nahi hai, har web game aise hi kaam karta hai. Database ki asal suraksha rules se hoti hai (upar wala point).
