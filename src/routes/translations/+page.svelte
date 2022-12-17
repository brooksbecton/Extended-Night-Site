<script>
  import "../../app.css";

  const EMAIL = "dirtydogsoftware88@gmail.com";
  const EMAIL_SUBJECT = "Translations | Extended Night Companion";
  const TRANSLATIONS_SPREADSHEET_COPY_URL =
    "https://docs.google.com/spreadsheets/d/1mjs2Lwx_Di-DzA8N0K5Y7r_gox0XA4ZJ1jxnWdDNjkw/copy?usp=sharing";
  const TRANSLATIONS_SPREADSHEET_VIEW_URL =
    "https://docs.google.com/spreadsheets/d/1mjs2Lwx_Di-DzA8N0K5Y7r_gox0XA4ZJ1jxnWdDNjkw/edit?usp=sharing";
</script>

<div class="Topography flex min-h-screen justify-center py-8">
  <div class="prose prose-invert flex w-5/6 flex-col rounded  py-4 xl:w-3/6 ">
    <a class="mb-4" href="/">Home</a>
    <h1>Translations</h1>
    <div>
      <p class="mt-0">
        The Extended Night Companion supports multiple languages on all of its
        screens. We try to keep all the translations in sync and accurate, but
        this can be difficult because my primary langauge is English
      </p>
      <p>
        Changing the text in the app is really easy! If members of the community
        can help with translations, we can make the app more accessible for
        non-English speakers.
      </p>
      <p class="mb-0">
        I've made a Google spreadsheet to hold the text for the app. Hopefully,
        this will help community members suggest edits or provide translations.
      </p>
    </div>
    <h2>Getting Started</h2>
    <h3>Small Changes</h3>
    <ol>
      <li>Click on the link below to <strong>view</strong> the translations</li>
      <ul>
        <li>
          <a href={TRANSLATIONS_SPREADSHEET_VIEW_URL} target="_blank"
            >Extended Night Companion Translations</a
          >
        </li>
      </ul>
      <li>Find the text to change</li>
      <li>
        Email <a href={`mailto:${EMAIL}?Subject="${EMAIL_SUBJECT}"`}>{EMAIL}</a>
      </li>
      <li>
        You can reference the cell's "key" or the column & row to help me find
        the text.
      </li>
      <li>Send the Email!</li>
    </ol>
    <h3>Big Changes</h3>
    <ol>
      <li>
        Click on the link below to <strong>make a copy</strong> of the translations
      </li>
      <ul>
        <li>
          <a href={TRANSLATIONS_SPREADSHEET_COPY_URL} target="_blank"
            >Extended Night Companion Translations</a
          >
        </li>
      </ul>
      <li>Make any changes you need to your copy</li>
      <li>
        Email <a href={`mailto:${EMAIL}?Subject="${EMAIL_SUBJECT}"`}>{EMAIL}</a>
      </li>
      <li>
        Let us know what cells you changed and attach your copy of the
        translations
      </li>
      <li>Send the Email!</li>
    </ol>
  </div>
</div>
