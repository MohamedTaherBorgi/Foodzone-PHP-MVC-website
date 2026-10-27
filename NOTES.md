# Developer Notes

## Asset Path Replacements
- **Client Pages**:
  - `url('` &rarr; `url('../public/client-assets/`
  - `href="` &rarr; `href="../public/client-assets/`
  - `src="` &rarr; `src="../public/client-assets/`
- **Dashboard (Admin)**:
  - `src="assets/` &rarr; `src="../public/admin-assets/`
  - `href="assets/` &rarr; `href="../public/admin-assets/`

## Layout Containers
- **Client Content**: inside `<div class="banner slider1 new-block"> </div>`
- **Admin Content**: inside `<div class="app-container"> </div>`

## PHP Sessions
PHP sessions are stored on the server and tied to a session ID, which is sent to the client via a cookie.
To read or write session data (e.g. `$_SESSION['user']`), ensure `session_start();` is called on every page that accesses session variables.
