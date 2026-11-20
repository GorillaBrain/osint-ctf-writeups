# No Oxygen — OSINT CTF Write-Up (Paria Diving Disaster)

**Challenge:** `No Oxygen` (50 pts)  
**Challmaker:** `MrGeneralQ`  
**Attachment:** `footage_cam.mp4`  
**Flag:** `OSINT{paria_diving_disaster_ttptp_queries@patnt.com}`

---

## Challenge Description

> Multiple individuals got involved and became a victim into a well known tragic incident. Attached you can find footage of the incident itself seconds before disaster struck.
>
> **Objective:** Identify the name of the incident associated with the video footage, the nearest UN/LOCODE of the nearest Depot number, and the contact email address associated with the location.
>
> **Format:** All lowercase, underscores for spaces (`OSINT{incident_name_unlocode_email}`).

---

## Step 1: Analyzing the Video Footage (`footage_cam.mp4`)

Extracting key frames from `footage_cam.mp4` (`486x360`, 30 FPS, 23.2 seconds) shows:
1. **0–2s:** Green underwater footage of a diver descending along a line/umbilical.
2. **4–6s:** A diver in a dark blue/purple wetsuit climbing into the bottom hatch of a white underwater chamber (hyperbaric habitat) where another diver is already inside.
3. **8–23s:** Bright interior lighting inside the habitat with diving hoses and regulators visible as the divers prepare to work on an underwater pipeline.

These frames match the GoPro helmet-camera footage recorded by commercial diver **Kazim Ali Jr.** seconds before the **Paria diving disaster** on **February 25, 2022**. Five divers contracted by Land and Marine Contracting Services (LMCS) were performing maintenance on a 30-inch underwater oil pipeline (**Sealine No. 36**) at **Berth #6** of the **Paria Fuel Trading Company Limited** marine terminal in **Pointe-à-Pierre, Trinidad and Tobago**, when a sudden differential pressure (Delta P) vortex pulled all five divers into the pipeline.

- **Incident Name:** `paria_diving_disaster`

---

## Step 2: Finding the Nearest UN/LOCODE

The incident took place at **Berth 6**, part of the **Paria Fuel Trading Company Limited** marine fuel terminal/depot at **Pointe-à-Pierre, Trinidad and Tobago** (`10.332° N, 61.486° W`).

Looking up Pointe-à-Pierre in maritime and UNECE location directories (`portcode.net`, `marinetraffic.com`, `cogoport.com`):
- **Port / Location:** Pointe-à-Pierre, Trinidad and Tobago
- **UN/LOCODE:** `TTPTP`
- **IMO GISIS Port Facility Number:** `TTPTP-0001` (*Paria Fuel Trading Co. Ltd.*)

- **UN/LOCODE (lowercase):** `ttptp`

---

## Step 3: Finding the Contact Email Address

The official website of **Paria Fuel Trading Company Limited** (`https://pariatt.co/contact-us/`) uses a web inquiry form rather than a general `info@` or `contact@` email address.

Checking the maritime port authority associated with **Port of Pointe-à-Pierre (`TTPTP`)** leads to the **Port Authority of Trinidad and Tobago (PATT)** (`https://www.patnt.com`), whose official general enquiries contact email address is:

- **Contact Email:** `queries@patnt.com`

---

## Final Flag

```text
OSINT{paria_diving_disaster_ttptp_queries@patnt.com}
```
