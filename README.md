# SafeSpace

SafeSpace is a small, browser-only prototype for people who feel concerned about privacy in a changing room or accommodation. It offers a camera bright-spot demo, a guided room checklist, optional local photo fingerprints, and a complaint draft.

## Open the project

This is a static site with no build step or backend. Open `index.html` in a browser, or serve this folder from a local static web server. Camera access generally requires HTTPS or localhost; browser and device permissions apply. The camera torch is not controlled by the app.

## Demo flow

1. Open `index.html` and choose **Scan**. Allow camera access, try **Start scan** and **Stop scan**, then choose to carry your observation into Capture.
2. To demonstrate a tracker alert flow, choose **I received a tracker alert on my phone**. This records your report of an OS alert; SafeSpace does not scan or verify a tracker.
3. On **Capture**, review the carried note, add an observation, select a sample photo, create a record, then download the JSON and original photo separately.
4. Open **Report draft**, select English or Hindi, fill in a fictional incident, optionally attach the JSON record, then review, copy, print, or search Maps for a police station near the place you entered.
5. Try **Room checklist**, mark areas, add sample photos, and download the inspection JSON and each photo separately.

Use fictional information and sample images for a public demo. Location is optional and can disclose sensitive information.

## Limits and privacy

- The scan flags a narrow pattern of bright spots in a camera image. It cannot identify hidden cameras and cannot establish that a room is safe.
- Wi-Fi device scanning and Bluetooth tracker detection are not implemented in this web prototype. The tracker-alert path records what the user says their phone reported; it is not a detector.
- Photos are processed locally by the browser and are not uploaded by this static prototype. The JSON record does not contain the photo; keep the original photo separately.
- A SHA-256 hash can detect whether a selected file differs from the file represented by a record. It does not establish authorship, time, location, or that the JSON record itself is authentic.
- Times and optional locations come from the user's device. Checklist selections are subjective observations.
- The complaint page creates a bilingual structured template, not AI output, verified legal advice, or a legal filing. It does not determine applicable laws or sections.
- Searching Maps sends the place text entered on the Report page to Google Maps only when the user clicks the search button.

## Files

- `index.html` — project landing page
- `home.html` — legacy link that redirects to the landing page
- `scan.html` — camera bright-spot demo and user-reported tracker-alert handoff
- `changing.html` — guided room checklist
- `capture.html` — photo fingerprint and evidence JSON
- `report.html` — editable complaint draft and print view
