<div align="center">
  <a href="https://readest.com?utm_source=github&utm_medium=referral&utm_campaign=readme" target="_blank">
    <img src="https://github.com/readest/readest/blob/main/apps/readest-app/src-tauri/icons/icon.png?raw=true" alt="Readest Logo" width="20%" />
  </a>
  <h1>Readest</h1>
  <br>

[Readest][link-website] is an open-source ebook reader designed for immersive and deep reading experiences. Built as a modern rewrite of [Foliate](https://github.com/johnfactotum/foliate), it leverages [Next.js 15](https://github.com/vercel/next.js) and [Tauri v2](https://github.com/tauri-apps/tauri) to deliver a smooth, cross-platform experience across macOS, Windows, Linux, Android, iOS, and the Web.

[![Website][badge-website]][link-website]
[![Web App][badge-web-app]][link-web-readest]
[![OS][badge-platforms]][link-website]
<br>
[![][badge-hellogithub]][link-hellogithub]
[![][badge-discord]][link-discord]
[![AGPL Licence][badge-license]](LICENSE)
[![Latest release][badge-release]][link-gh-releases]
[![Last commit][badge-last-commit]][link-gh-commits]
[![Commits][badge-commit-activity]][link-gh-pulse]

</div>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#planned-features">Planned Features</a> •
  <a href="#screenshots">Screenshots</a> •
  <a href="#downloads">Downloads</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#troubleshooting">Troubleshooting</a> •
  <a href="#license">License</a>
</p>

<div align="center">
  <a href="https://readest.com" target="_blank">
    <img src="./data/screenshots/landing_all_platforms.png" alt="Readest Banner" width="100%" />
  </a>
</div>

## Features

<div align="left">✅ Implemented</div>

| **Feature**                             | **Description**                                                                                | **Status** |
| --------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------- |
| **Multi-Format Support**                | Support EPUB, MOBI, KF8 (AZW3), FB2, CBZ, TXT, PDF (experimental)                              | ✅         |
| **Scroll/Page View Modes**              | Switch between scrolling or paginated reading modes.                                           | ✅         |
| **Full-Text Search**                    | Search across the entire book to find relevant sections.                                       | ✅         |
| **Annotations and Highlighting**        | Add highlights, bookmarks, and notes to enhance your reading experience.                       | ✅         |
| **Excerpt Text for Note-Taking**        | Easily excerpt text from books for detailed notes and analysis.                                | ✅         |
| **Dictionary/Wikipedia Lookup**         | Instantly look up words and terms when reading.                                                | ✅         |
| **Translate with DeepL**                | Translate selected text instantly using DeepL for accurate translations.                       | ✅         |
| **[Parallel Read][link-parallel-read]** | Read two books or documents simultaneously in a split-screen view.                             | ✅         |
| **Customize Font and Layout**           | Adjust font, layout, theme mode, and theme colors for a personalized experience.               | ✅         |
| **File Association and Open With**      | Quickly open files in Readest in your file browser with one-click.                             | ✅         |
| **Sync across Platforms**               | Synchronize book files, reading progress, notes, and bookmarks across all supported platforms. | ✅         |
| **Text-to-Speech (TTS) Support**        | Enable text-to-speech functionality for a more accessible reading experience.                  | ✅         |
| **Library Management**                  | Organize, sort, and manage your entire ebook library.                                          | ✅         |

## Planned Features

<div align="left">🛠 Building</div>
<div align="left">🔄 Planned</div>

| **Feature**                     | **Description**                                                                            | **Priority** |
| ------------------------------- | ------------------------------------------------------------------------------------------ | ------------ |
| **AI-Powered Summarization**    | Generate summaries of books or chapters using AI for quick insights.                       | 🛠           |
| **Sync with Koreader**          | Synchronize reading progress, notes, and bookmarks with [Koreader][link-koreader] devices. | 🔄           |
| **Keyboard Navigation**         | Implement vimium-style keybindings for book navigation.                                    | 🔄           |
| **Support OPDS/Calibre**        | Integrate OPDS/Calibre to access online libraries and catalogs.                            | 🔄           |
| **Audiobook Support**           | Extend functionality to play and manage audiobooks.                                        | 🔄           |
| **Handwriting Annotations**     | Add support for handwriting annotations using a pen on compatible devices.                 | 🔄           |
| **Advanced Reading Stats**      | Track reading time, pages read, and more for detailed insights.                            | 🔄           |
| **In-Library Full-Text Search** | Search across your entire ebook library to find topics and quotes.                         | 🔄           |

Stay tuned for continuous improvements and updates! Contributions and suggestions are always welcome—let's build the ultimate reading experience together. 😊

## Screenshots

![Annotations](./data/screenshots/annotations.png)

![DeepL](./data/screenshots/deepl.png)

![TTS](./data/screenshots/tts_speak_aloud.png)

![Footnote](./data/screenshots/footnote_popover.png)

![Wikipedia](./data/screenshots/wikipedia_vertical.png)

![Themeing Dark Mode](./data/screenshots/theming_dark_mode.png)

---

## Downloads

The Readest app is available for download! 🥳 🚀

- macOS / iOS / iPadOS : Search for "Readest" on the [App Store][link-appstore], also available on TestFlight for beta test (send your Apple ID to readestapp@gmail.com to request access).
- Windows / Linux / Android: Visit [https://readest.com][link-website] or the [Releases on GitHub][link-gh-releases].
- Web: Visit [https://web.readest.com][link-web-readest].

## Requirements

- **Node.js** and **pnpm** for Next.js development
- **Rust** and **Cargo** for Tauri development

For the best experience to build Readest for yourself, use a recent version of Node.js and Rust. Refer to the [Tauri documentation](https://v2.tauri.app/start/prerequisites/) for details on setting up the development environment prerequisites on different platforms.

```bash
nvm install v22
nvm use v22
npm install -g pnpm
rustup update
```

## Getting Started

To get started with Readest, follow these steps to clone and build the project.

### 1. Clone the Repository

```bash
git clone https://github.com/readest/readest.git
cd readest
git submodule update --init --recursive
```

### 2. Install Dependencies

```bash
# might need to rerun this when code is updated
pnpm install
# copy pdfjs-dist to Next.js public directory
pnpm --filter @readest/readest-app setup-pdfjs
```

### 3. Verify Dependencies Installation

To confirm that all dependencies are correctly installed, run the following command:

```bash
pnpm tauri info
```

This command will display information about the installed Tauri dependencies and configuration on your platform. Note that the output may vary depending on the operating system and environment setup. Please review the output specific to your platform for any potential issues.

For Windows targets, "Build Tools for Visual Studio 2022" (or a higher edition of Visual Studio) and the "Desktop development with C++" workflow must be installed. For Windows ARM64 targets, the "VS 2022 C++ ARM64 build tools" and "C++ Clang Compiler for Windows" components must be installed. And make sure `clang` can be found in the path by adding `C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools\VC\Tools\Llvm\x64\bin` for example in the environment variable `Path`.

### 4. Set Up Supabase for Sync Functionality

The app uses Supabase for synchronization of reading progress, bookmarks, notes, and preferences across devices.

#### 4.1. Set Environment Variables

Create a `.env` file in the project root directory (or copy from `.env.example` if it exists) and add the following Supabase-related variables:

```
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
```

- `NEXT_PUBLIC_SUPABASE_URL`: The URL of your Supabase project (e.g., `https://your-project-id.supabase.co`)
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`: The anonymous key for your Supabase project (found in your Supabase project settings under API)

#### 4.2. Set Up Supabase Database Tables

You need to create the necessary tables in your Supabase project. You can use the Supabase SQL Editor to run the following SQL commands:

```sql
-- Books table to store book metadata and progress
create table public.books (
  user_id uuid not null,
  book_hash text not null,
  format text null, -- 'EPUB' | 'PDF' | 'MOBI' | 'CBZ' | 'FB2' | 'FBZ'
  title text null,
  author text null,
  "group" text null,
  tags text[] null,
  created_at timestamp with time zone null default now(),
  updated_at timestamp with time zone null default now(),
  deleted_at timestamp with time zone null,
  uploaded_at timestamp with time zone null,
  progress integer[] null,
  group_id text null,
  group_name text null,
  constraint books_pkey primary key (user_id, book_hash),
  constraint books_user_id_fkey foreign KEY (user_id) references auth.users (id) on delete CASCADE
) TABLESPACE pg_default;

ALTER TABLE public.books ENABLE ROW LEVEL SECURITY;

CREATE POLICY select_books ON public.books
  FOR SELECT to authenticated USING ((select auth.uid()) = user_id);
CREATE POLICY insert_books ON public.books
  FOR INSERT to authenticated WITH CHECK ((select auth.uid()) = user_id);
CREATE POLICY update_books ON public.books
  FOR UPDATE to authenticated USING ((select auth.uid()) = user_id);
CREATE POLICY delete_books ON public.books
  FOR DELETE to authenticated USING ((select auth.uid()) = user_id);

-- Book configurations table to store view settings and progress
create table public.book_configs (
  user_id uuid not null,
  book_hash text not null,
  location text null,
  progress jsonb null,
  search_config jsonb null,
  view_settings jsonb null,
  created_at timestamp with time zone null default now(),
  updated_at timestamp with time zone null default now(),
  deleted_at timestamp with time zone null,
  constraint book_configs_pkey primary key (user_id, book_hash),
  constraint book_configs_user_id_fkey foreign KEY (user_id) references auth.users (id) on delete CASCADE
) TABLESPACE pg_default;

ALTER TABLE public.book_configs ENABLE ROW LEVEL SECURITY;

CREATE POLICY select_book_configs ON public.book_configs
  FOR SELECT to authenticated USING ((select auth.uid()) = user_id);
CREATE POLICY insert_book_configs ON public.book_configs
  FOR INSERT to authenticated WITH CHECK ((select auth.uid()) = user_id);
CREATE POLICY update_book_configs ON public.book_configs
  FOR UPDATE to authenticated USING ((select auth.uid()) = user_id);
CREATE POLICY delete_book_configs ON public.book_configs
  FOR DELETE to authenticated USING ((select auth.uid()) = user_id);

-- Book notes table to store annotations, highlights, and bookmarks
create table public.book_notes (
  user_id uuid not null,
  book_hash text not null,
  id text not null,
  type text null,
  cfi text null,
  text text null,
  style text null,
  color text null,
  note text null,
  created_at timestamp with time zone null default now(),
  updated_at timestamp with time zone null default now(),
  deleted_at timestamp with time zone null,
  constraint book_notes_pkey primary key (user_id, book_hash, id),
  constraint book_notes_user_id_fkey foreign KEY (user_id) references auth.users (id) on delete CASCADE
) TABLESPACE pg_default;

ALTER TABLE public.book_notes ENABLE ROW LEVEL SECURITY;

CREATE POLICY select_book_notes ON public.book_notes
  FOR SELECT to authenticated USING ((select auth.uid()) = user_id);
CREATE POLICY insert_book_notes ON public.book_notes
  FOR INSERT to authenticated WITH CHECK ((select auth.uid()) = user_id);
CREATE POLICY update_book_notes ON public.book_notes
  FOR UPDATE to authenticated USING ((select auth.uid()) = user_id);
CREATE POLICY delete_book_notes ON public.book_notes
  FOR DELETE to authenticated USING ((select auth.uid()) = user_id);

-- Files table to store book files
create table public.files (
  id uuid not null default gen_random_uuid (),
  user_id uuid not null,
  book_hash text null,
  file_key text not null,
  file_size bigint not null,
  created_at timestamp with time zone null default now(),
  deleted_at timestamp with time zone null,
  constraint files_pkey primary key (id),
  constraint files_file_key_key unique (file_key),
  constraint files_user_id_fkey foreign KEY (user_id) references auth.users (id) on delete CASCADE
) TABLESPACE pg_default;

-- Add indexes for efficient querying
create index idx_files_user_id_deleted_at
on public.files (user_id, deleted_at);

create index idx_files_file_key
on public.files (file_key);

create index idx_files_file_key_deleted_at
on public.files (file_key, deleted_at);

-- Enable RLS on the files table
alter table public.files enable row level security;

create policy "Users can view their own active files"
on public.files
for select
using (
  auth.uid() = user_id and deleted_at is null
);

create policy "Users can soft-delete their own files"
on public.files
for update
using (
  auth.uid() = user_id
)
with check (
  deleted_at is null or deleted_at > now()
);

create policy "Users can delete their own files permanently"
on public.files
for delete
using (
  auth.uid() = user_id
);
```

#### 4.3. Alternative: Local Supabase Development

For local development, you can use Supabase CLI:

1. Install Supabase CLI: `npm install -g supabase`
2. Start local Supabase: `supabase start`
3. Copy the provided URL and anon key to your `.env` file
4. Run the SQL script: `supabase db reset` (after saving the above SQL in `supabase/migrations`)

### 5. Build for Development

```bash
# Start development for the Tauri app
pnpm tauri dev
# or start development for the Web app
pnpm dev-web
```

For Android:

```bash
# Initialize the Android environment (run once)
pnpm tauri android init

pnpm tauri android dev
# or if you want to dev on a real device
pnpm tauri android dev --host
```

For iOS:

```bash
# Set up the iOS environment (run once)
pnpm tauri ios init

pnpm tauri ios dev
# or if you want to dev on a real device
pnpm tauri ios dev --host
```

### 6. Build for Production

```bash
pnpm tauri build
pnpm tauri android build
pnpm tauri ios build
```

### 7. Setup dev environment with Nix

If you have Nix installed, you can leverage flake to enter a development shell
with all the necessary dependencies:

```bash
nix develop ./ops  # enter a dev shell for the web app
nix develop ./ops#ios # enter a dev shell for the ios app
nix develop ./ops#android # enter a dev shell for the android app
```

### 8. More information

Please check the [wiki][link-gh-wiki] of this project for more information on development.

## Troubleshooting

### 1. Readest Won't Launch on Windows (Missing Edge WebView2 Runtime)

**Symptom**

- When you double-click readest.exe, nothing happens. No window appears, and Task Manager does not show the process.
- This can affect both the standard installer and the portable version.

**Cause**

- Microsoft Edge WebView2 Runtime is either missing, outdated, or improperly installed on your system. Readest depends on WebView2 to render the interface on Windows.

**How to Fix**

1. Check if WebView2 is installed
   - Open "Add or Remove Programs" (a.k.a. Apps & features) on Windows. Look for "Microsoft Edge WebView2 Runtime."
2. Install or Update WebView2
   - Download the WebView2 Runtime directly from Microsoft: [link](https://developer.microsoft.com/en-us/microsoft-edge/webview2?form=MA13LH).
   - If you prefer an offline installer, download the offline package and run it as an Administrator.
3. Re-run Readest
   - After installing/updating WebView2, launch readest.exe again.
   - If you still encounter problems, reboot your PC and try again.

**Additional Tips**

- If reinstalling once doesn't work, uninstall Edge WebView2 completely, then reinstall it with Administrator privileges.
- Verify your Windows installation has the latest updates from Microsoft.

**Still Stuck?**

- See Issue [readest/readest#358](https://github.com/readest/readest/issues/358) for further details, or head over to our [Discord][link-discord] server and open a support discussion with detailed logs of your environment and the steps you've taken.

## Contributors

Readest is open-source, and contributions are welcome! Feel free to open issues, suggest features, or submit pull requests. Please **review our [contributing guidelines](CONTRIBUTING.md) before you start**. We also welcome you to join our [Discord][link-discord] community for either support or contributing guidance.

<a href="https://github.com/readest/readest/graphs/contributors">
  <p align="left">
    <img width="500" src="https://contrib.rocks/image?repo=readest/readest" alt="A table of avatars from the project's contributors" />
  </p>
</a>

## License

Readest is free software: you can redistribute it and/or modify it under the terms of the [GNU Affero General Public License](https://www.gnu.org/licenses/agpl-3.0.html) as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version. See the [LICENSE](LICENSE) file for details.

The following libraries and frameworks are used in this software:

- [foliate-js](https://github.com/johnfactotum/foliate-js), which is MIT licensed.
- [zip.js](https://github.com/gildas-lormeau/zip.js), which is licensed under the BSD-3-Clause license.
- [fflate](https://github.com/101arrowz/fflate), which is MIT licensed.
- [PDF.js](https://github.com/mozilla/pdf.js), which is licensed under Apache License 2.0.
- [daisyUI](https://github.com/saadeghi/daisyui), which is MIT licensed.
- [next.js](https://github.com/vercel/next.js), which is MIT licensed.
- [react-icons](https://github.com/react-icons/react-icons), which has various open-source licenses.
- [react](https://github.com/facebook/react), which is MIT licensed.
- [tauri](https://github.com/tauri-apps/tauri), which is MIT licensed.

The following fonts are utilized in this software, either bundled within the application or provided through web fonts:

[Bitter](https://fonts.google.com/?query=Bitter), [Fira Code](https://fonts.google.com/?query=Fira+Code), [Literata](https://fonts.google.com/?query=Literata), [Merriweather](https://fonts.google.com/?query=Merriweather), [Noto Sans](https://fonts.google.com/?query=Noto+Sans), [Roboto](https://fonts.google.com/?query=Roboto), [LXGW WenKai](https://github.com/lxgw/LxgwWenKai), [MiSans](https://hyperos.mi.com/font/en/), [Source Han](https://github.com/adobe-fonts/source-han-sans/), [WenQuanYi Micro Hei](http://wenq.org/wqy2/)

---

<div align="center" style="color: gray;">Happy reading with Readest!</div>

[badge-website]: https://img.shields.io/badge/website-readest.com-orange
[badge-web-app]: https://img.shields.io/badge/read%20online-web.readest.com-orange
[badge-license]: https://img.shields.io/github/license/readest/readest?color=teal
[badge-release]: https://img.shields.io/github/release/readest/readest?color=green
[badge-platforms]: https://img.shields.io/badge/platforms-macOS%2C%20Windows%2C%20Linux%2C%20Android%2C%20iOS%2C%20Web%2C%20PWA-green
[badge-last-commit]: https://img.shields.io/github/last-commit/readest/readest?color=green
[badge-commit-activity]: https://img.shields.io/github/commit-activity/m/readest/readest
[badge-discord]: https://img.shields.io/discord/1314226120886976544?color=5865F2&label=discord&labelColor=black&logo=discord&logoColor=white&style=flat-square
[badge-hellogithub]: https://abroad.hellogithub.com/v1/widgets/recommend.svg?rid=8a5b6ade2aee461a8bd94e59200682a7&claim_uid=eRLUbPOy2qZtDgw&theme=small
[link-appstore]: https://apps.apple.com/app/apple-store/id6738622779?pt=127463130&ct=github&mt=8
[link-website]: https://readest.com?utm_source=github&utm_medium=referral&utm_campaign=readme
[link-web-readest]: https://web.readest.com
[link-gh-releases]: https://github.com/readest/readest/releases
[link-gh-commits]: https://github.com/readest/readest/commits/main
[link-gh-pulse]: https://github.com/readest/readest/pulse
[link-gh-wiki]: https://github.com/readest/readest/wiki
[link-discord]: https://discord.gg/gntyVNk3BJ
[link-parallel-read]: https://readest.com/#parallel-read
[link-koreader]: https://github.com/koreader/koreader
[link-hellogithub]: https://hellogithub.com/repository/8a5b6ade2aee461a8bd94e59200682a7
