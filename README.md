# sorter-ui

Phone-first control panel for the Tor2cloud torrent -> FileLu sorter.
Static page on GitHub Pages, backed by a Cloudflare worker.

- Passcode-gated: every view and action needs the passcode.
- Paste one or many links (one per line) or drop .torrent files. The
  backend reads what each link actually serves: torrent bytes go to
  Seedr, anything else fetches straight to FileLu.
- Job cards show queue position, live Seedr %, and FileLu fetch %.
- The queue lives in the private pipeline repo's issues, never inside
  Seedr: jobs pack into the 5 GB allowance, held jobs promote themselves,
  and a waiting job can be cancelled with its X. Active jobs are never
  interrupted.
- Names: movies become "Name (Year)", TV episodes keep their SxxEyy tag.
  Language routes the folder (English / Tamil / Malayalam). Direct links
  can be any file type - audio, docs, and apps route to their own
  folders.
- Closed jobs hide by default; the filter chips show done / failed /
  cancelled.

The pipeline itself lives in the private `torrent-filelu-sorter` repo.
