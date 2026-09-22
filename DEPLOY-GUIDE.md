# VB Civil Solution — Online Version (GitHub + Supabase + Vercel)

இந்த folder-ல `index.html` ஒரே ஒரு file தான் இருக்கு. அது போதும்.

---

## 1. Supabase — ஏற்கனவே ready ✅

நான் உங்க Supabase account-ல set up பண்ணிட்டேன். நீங்க எதுவும் செய்ய வேண்டாம்.

| | |
|---|---|
| Project name | `vb-civil-solution` |
| Region | Mumbai (ap-south-1) |
| Table | `app_state` |
| Cost | **₹0 / month** (free tier) |

Project URL மற்றும் key ஏற்கனவே `index.html`-க்குள்ள சேர்த்தாச்சு.

---

## 2. GitHub-ல upload பண்றது

1. https://github.com → **New repository**
2. Repository name: `vb-civil-solution` (எந்த பேரும் ஓகே)
3. **Private** அல்லது **Public** — எதுவும் வேலை செய்யும்
4. **Create repository**
5. அடுத்த page-ல **"uploading an existing file"** link-ஐ click பண்ணுங்க
6. `index.html` file-ஐ drag & drop பண்ணி **Commit changes**

> ⚠️ File பேரை `index.html`-ஆவே வைங்க. மாத்தினா Vercel-ல வேலை செய்யாது.

---

## 3. Vercel-ல deploy பண்றது

1. https://vercel.com → **Add New… → Project**
2. **Import Git Repository** → மேல create பண்ண repo-வை select பண்ணுங்க
3. Framework Preset: **Other** (தானா select ஆகும்)
4. வேற எந்த setting-ஐயும் மாத்த வேண்டாம் — **Deploy** அழுத்துங்க
5. 30 வினாடில ஒரு link கிடைக்கும்:
   `https://vb-civil-solution.vercel.app`

அவ்வளவுதான். அந்த link-ஐ எந்த phone/laptop-ல திறந்தாலும் software வேலை செய்யும்.

**அப்புறம் ஏதாவது மாத்தணும்னா:** GitHub-ல `index.html`-ஐ update பண்ணா போதும், Vercel தானா re-deploy பண்ணிடும்.

---

## 4. Exe-ல இருக்குற பழைய data-வை online-க்கு கொண்டு வர்றது

1. **Exe-ஐ திறங்க** → **Backup** tab → **⬇ Download Full Backup (JSON)**
2. **Vercel link-ஐ திறங்க** → **Backup** tab → **Import/Restore** → அந்த JSON file-ஐ select பண்ணுங்க
3. Confirm பண்ணுங்க. Data cloud-ல ஏறி, page தானா reload ஆகும்.

---

## எப்படி வேலை செய்யுது

- Data முழுசும் Supabase-ல ஒரு JSON-ஆ save ஆகுது
- நீங்க எதை add/edit பண்ணாலும், சுமார் 1 வினாடியில cloud-ல சேவ் ஆகும்
- வலது கீழ மூலையில **sync status** தெரியும்:
  - ✅ **Saved to cloud** — சேவ் ஆயிடுச்சு
  - ⏳ **Saving…** — சேவ் ஆயிட்டு இருக்கு
  - ⚠️ **Offline — not saved** — internet இல்ல (data local-ல பத்திரமா இருக்கும், net வந்ததும் தானா ஏறிடும்)
  - 🔴 **Another device changed the data** — கீழ பாருங்க

### 🔴 இரண்டு device-ல ஒரே நேரத்துல வேலை செஞ்சா

உதா: laptop-லயும் phone-லயும் ஒரே நேரத்துல app திறந்து வேலை செஞ்சா.

ஒரு device சேவ் பண்ணதுக்கு அப்புறம் இன்னொரு device சேவ் பண்ண முயற்சி பண்ணா, **அது தானா overwrite பண்ணாது**. பதிலா சிவப்பு pill காட்டும். அத **click** பண்ணா உங்களுக்கு இரண்டு option கிடைக்கும்:

- **OK** = என்னோட version-ஐ வெச்சுக்கோ (அந்த device-ல செஞ்சது போயிடும்)
- **Cancel** = என்னுது வேண்டாம், அவங்க version-ஐ load பண்ணு

> ⚠️ பாதுகாப்பா இருக்க: முடிஞ்சவரை **ஒரு நேரத்துல ஒரு device-ல மட்டும்** வேலை செய்யுங்க.

### Internet இல்லாதப்போ செஞ்ச வேலை

Net இல்லாதப்போ நீங்க செஞ்ச மாற்றங்கள் அந்த device-ல பத்திரமா இருக்கும். அடுத்த தடவை app திறக்கும்போது, cloud-ல வேற data இருந்தா, **எதை வெச்சுக்கணும்னு உங்க கிட்ட கேட்கும்** — தானா அழிச்சுடாது.
- **Internet போனாலும் app வேலை செய்யும்** — browser-ல ஒரு local copy இருக்கும்
- சேவ் ஆகாம இருக்கும்போது tab-ஐ close பண்ண முயற்சி பண்ணா, browser எச்சரிக்கை காட்டும்

---

## ⚠️ முக்கியம் — Login இல்ல

இப்போதைக்கு இந்த app-ல **login/password கிடையாது**. அதாவது Vercel link யார் கிட்ட போனாலும், அவங்க உங்க முழு billing data-வையும் பார்க்கலாம், மாத்தலாம், delete பண்ணலாம்.

**தற்காலிகமா பாதுகாப்பா இருக்க:**
- Vercel link-ஐ யார் கிட்டயும் share பண்ணாதீங்க
- Vercel Project Settings → Deployment Protection → **Password Protection** on பண்ணலாம் (Pro plan)

**நிரந்தர தீர்வு:** Supabase Auth (email + password login) சேர்க்கணும். கேளுங்க, சேர்த்து தர்றேன்.

---

## Backup பழக்கம்

Cloud-ல இருந்தாலும், மாசத்துக்கு ஒரு தடவை **Backup tab → Download Full Backup** பண்ணி ஒரு copy-ஐ உங்க computer-ல வெச்சுக்கோங்க. தப்பா delete ஆனா திரும்ப கொண்டு வர உதவும்.
