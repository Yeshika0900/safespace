# SafeSpace

SafeSpace is a small, browser-only prototype for people who feel concerned about privacy in a changing room or accommodation. It offers a camera bright-spot demo, a guided room checklist, optional local photo fingerprints, and a complaint draft.

## Open the project

This is a static site with no build step or backend. Open `home.html` in a browser, or serve this folder from a local static web server. Camera access generally requires HTTPS or localhost; browser and device permissions apply. The camera torch is not controlled by the app.

## Demo flow

1. Open `home.html` and choose **Scan**. Allow camera access, then try **Start scan** and **Stop scan**.
2. Open **Room checklist**, mark a few areas, select a sample image, and download the inspection JSON and photo separately.
3. Open **Capture**, select a sample photo, download both its JSON record and original photo, then reload the page and use the saved record to verify the photo fingerprint.
4. Open **Report draft**, fill in a fictional incident and optionally attach the JSON record. Review the draft before printing.

Use fictional information and sample images for a public demo. Location is optional and can disclose sensitive information.

## Limits and privacy

- The scan flags a narrow pattern of bright spots in a camera image. It cannot identify hidden cameras and cannot establish that a room is safe.
- Photos are processed locally by the browser and are not uploaded by this static prototype. The JSON record does not contain the photo; keep the original photo separately.
- A SHA-256 hash can detect whether a selected file differs from the file represented by a record. It does not establish authorship, time, location, or that the JSON record itself is authentic.
- Times and optional locations come from the user's device. Checklist selections are subjective observations.
- The complaint page creates an editable draft, not a verified legal filing or legal advice. Check official support information before relying on it.

## Files

- `home.html` — project landing page
- `index.html` — camera bright-spot demo
- `changing.html` — guided room checklist
- `capture.html` — photo fingerprint and evidence JSON
- `report.html` — editable complaint draft and print view
