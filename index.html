<!doctype html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Volunteer-Hours Ledger</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&family=Inter:wght@400;450;500;600&display=swap" rel="stylesheet" />
<style>
  :root {
    --paper:#F4F5F0; --panel:#FBFBF7; --ink:#1C2A24; --ink-soft:#4A5A52;
    --rule:#DADFD3; --verified:#2F6B4F; --verified-bg:#EAF2EC; --flag:#B4531A; --flag-bg:#FBF0E6;
    --display:'Space Grotesk',system-ui,sans-serif; --body:'Inter',system-ui,sans-serif;
    --mono:'IBM Plex Mono',ui-monospace,monospace;
  }
  * { box-sizing:border-box; }
  body { margin:0; background:var(--paper); color:var(--ink); font-family:var(--body);
         -webkit-font-smoothing:antialiased; min-height:100vh; }
  .wrap { max-width:820px; margin:0 auto; padding:clamp(20px,4vw,44px); }
  .eyebrow { font-family:var(--mono); font-size:12px; letter-spacing:.14em; text-transform:uppercase;
             color:var(--verified); margin-bottom:8px; }
  h1 { font-family:var(--display); font-size:clamp(26px,5vw,38px); font-weight:700; margin:0;
       letter-spacing:-.02em; line-height:1.05; }
  .lede { font-size:15px; color:var(--ink-soft); margin:12px 0 0; max-width:600px; line-height:1.55; }

  .settings { display:flex; flex-wrap:wrap; gap:10px; align-items:flex-end; margin:24px 0 4px;
              padding:14px 16px; background:var(--panel); border:1px solid var(--rule); border-radius:10px; }
  .settings .grow { flex:1; min-width:180px; }
  .settings label { display:block; font-family:var(--mono); font-size:10px; letter-spacing:.05em;
                    text-transform:uppercase; color:var(--ink-soft); margin-bottom:5px; }
  .hint { font-family:var(--body); font-size:12px; color:var(--ink-soft); margin:8px 0 0; }
  .hint a { color:var(--verified); }
  .keyok { font-family:var(--mono); font-size:11px; color:var(--verified); }

  input, select { width:100%; font-family:var(--body); font-size:14px; color:var(--ink);
    background:#fff; border:1px solid var(--rule); border-radius:7px; padding:9px 11px; outline:none; }
  input:focus, select:focus { border-color:var(--ink); }

  .tabs { display:flex; gap:4px; border-bottom:1px solid var(--rule); margin:26px 0; }
  .tab { font-family:var(--display); font-weight:600; font-size:14px; color:var(--ink-soft);
    background:none; border:none; border-bottom:2px solid transparent; padding:10px 14px;
    margin-bottom:-1px; cursor:pointer; }
  .tab.active { color:var(--ink); border-bottom-color:var(--ink); }

  .form-grid { display:grid; grid-template-columns:1fr 1fr; gap:0 16px; max-width:560px; }
  .field { margin-bottom:14px; }
  .field label { display:block; font-family:var(--mono); font-size:11px; letter-spacing:.05em;
    text-transform:uppercase; color:var(--ink-soft); margin-bottom:6px; }

  .btn { font-family:var(--display); font-weight:600; font-size:13.5px; padding:9px 16px; border-radius:6px;
    cursor:pointer; color:var(--paper); background:var(--ink); border:1.5px solid var(--ink); transition:opacity .15s; }
  .btn:disabled { opacity:.5; cursor:not-allowed; }
  .btn-ghost { background:transparent; color:var(--ink); }
  .btn-verified { background:var(--verified); border-color:var(--verified); color:var(--paper); }
  .btn-ghost.btn-flag { background:transparent; color:var(--flag); border-color:var(--flag); }

  .lede-sm { font-size:14px; color:var(--ink-soft); margin:0 0 18px; max-width:560px; }

  .result { margin-top:18px; max-width:560px; border-radius:8px; padding:14px 16px; }
  .result.ok { background:var(--verified-bg); border:1px solid #2F6B4F33; }
  .result.review { background:var(--flag-bg); border:1px solid #B4531A33; }
  .result h4 { font-family:var(--display); font-size:14px; margin:0; }
  .result.ok h4 { color:var(--verified); } .result.review h4 { color:var(--flag); }
  .result p { font-size:13px; color:var(--ink-soft); margin:8px 0 0; }

  .tags { display:flex; gap:6px; flex-wrap:wrap; margin-top:8px; }
  .tag { font-family:var(--mono); font-size:10px; text-transform:uppercase; letter-spacing:.05em;
    color:var(--flag); border:1px solid #B4531A44; border-radius:3px; padding:2px 6px; }

  .error { margin-top:16px; max-width:560px; font-size:14px; color:var(--flag);
    background:var(--flag-bg); border:1px solid #B4531A33; border-radius:8px; padding:12px 16px; }

  .queue-item { display:flex; gap:14px; align-items:flex-start; padding:14px 16px; background:var(--panel);
    border:1px solid var(--rule); border-radius:0 8px 8px 0; margin-bottom:10px; }
  .queue-item.ok { border-left:3px solid var(--verified); }
  .queue-item.review { border-left:3px solid var(--flag); }
  .qi-name { font-weight:600; font-size:14.5px; }
  .qi-meta { font-family:var(--mono); font-weight:400; color:var(--ink-soft); margin-left:10px; font-size:12px; }
  .qi-activity { font-size:13px; color:var(--ink-soft); margin-top:3px; }
  .qi-note { font-size:13px; margin-top:6px; }
  .qi-note.review { color:var(--flag); } .qi-note.ok { color:var(--verified); }
  .qi-actions { display:flex; flex-direction:column; gap:8px; }

  .section-label { font-family:var(--mono); font-size:11px; letter-spacing:.1em; text-transform:uppercase;
    color:var(--ink-soft); margin-bottom:12px; display:flex; align-items:center; gap:10px; }
  .section-label span { flex:1; height:1px; background:var(--rule); }

  .summary { display:flex; align-items:baseline; gap:14px; padding:16px 20px; background:var(--panel);
    border:1px solid var(--rule); border-radius:8px; margin-bottom:22px; }
  .summary .big { font-family:var(--mono); font-size:34px; font-weight:600; color:var(--verified); line-height:1; }
  .summary .lbl { font-size:13px; color:var(--ink-soft); }

  table { width:100%; border-collapse:collapse; }
  .tbl-wrap { border:1px solid var(--rule); border-radius:8px; overflow:hidden; margin-bottom:26px; }
  th { font-family:var(--mono); font-size:11px; letter-spacing:.06em; text-transform:uppercase;
    color:var(--ink-soft); padding:10px 16px; border-bottom:1px solid var(--rule); background:var(--panel); text-align:left; }
  th.num, td.num { text-align:right; }
  td { padding:12px 16px; border-bottom:1px solid var(--rule); font-size:14px; }
  tr:last-child td { border-bottom:none; }
  td.name { font-weight:500; } td.hrs { font-family:var(--mono); font-weight:600; color:var(--verified); }
  td.count { font-family:var(--mono); font-size:13px; color:var(--ink-soft); }

  .entries { border:1px solid var(--rule); border-radius:8px; overflow:hidden; }
  .entry-row { display:flex; gap:12px; align-items:baseline; padding:10px 16px; border-bottom:1px solid var(--rule); }
  .entry-row:last-child { border-bottom:none; }
  .er-name { font-weight:500; font-size:13.5px; min-width:130px; }
  .er-date { font-family:var(--mono); font-size:12px; color:var(--ink-soft); min-width:90px; }
  .er-hrs { font-family:var(--mono); font-size:12.5px; color:var(--verified); font-weight:600; min-width:40px; }
  .er-act { font-size:13px; color:var(--ink-soft); flex:1; }

  .empty { text-align:center; padding:48px 24px; border:1px dashed var(--rule); border-radius:10px; }
  .empty h3 { font-family:var(--display); font-size:17px; margin:0; }
  .empty p { font-size:14px; color:var(--ink-soft); margin:6px auto 0; max-width:360px; line-height:1.5; }

  .footer { margin-top:40px; padding-top:16px; border-top:1px solid var(--rule);
    font-family:var(--mono); font-size:11px; color:var(--ink-soft); letter-spacing:.03em; line-height:1.6; }
</style>
</head>
<body>
<div id="app"></div>

<script>
(function () {
  "use strict";

  // ---- storage -------------------------------------------------------------
  var K = { pending:"vhl_pending", approved:"vhl_approved", key:"vhl_apikey", model:"vhl_model" };
  function load(k, fb) { try { var v = localStorage.getItem(k); return v ? JSON.parse(v) : fb; } catch (e) { return fb; } }
  function save(k, v) { try { localStorage.setItem(k, JSON.stringify(v)); } catch (e) {} }

  var state = {
    tab: "submit",
    pending: load(K.pending, []),
    approved: load(K.approved, []),
    apiKey: localStorage.getItem(K.key) || "",
    model: localStorage.getItem(K.model) || "claude-sonnet-5",
    submitMsg: null
  };

  var FLAG_LABELS = {
    duplicate:"Duplicate", impossible_hours:"Impossible hours", missing_field:"Missing field",
    activity_mismatch:"Hours don't match activity", vague_activity:"Vague activity", other:"Needs a look"
  };

  // ---- helpers -------------------------------------------------------------
  function esc(s) {
    return String(s == null ? "" : s).replace(/[&<>"']/g, function (c) {
      return { "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;" }[c];
    });
  }
  function id() { return Date.now() + "-" + Math.round(Math.random() * 1e6); }

  // ---- Claude check on a single entry --------------------------------------
  async function checkEntry(entry) {
    var prior = state.approved.filter(function (a) {
      return a.name.trim().toLowerCase() === entry.name.trim().toLowerCase();
    });
    var history = prior.slice(-10).map(function (e) {
      return "- " + e.date + ": " + e.hours + "h, " + e.activity;
    }).join("\n") || "(none on record)";

    var system = "You are a meticulous volunteer-hours reviewer for a nonprofit that reports fiscal " +
      "volunteer hours to a national partner. Judge a single new submission. Return ONLY valid JSON, " +
      "no prose, no markdown fences.";

    var user =
      "New submission from a volunteer:\n" +
      "name: " + (entry.name || "(blank)") + "\n" +
      "date: " + (entry.date || "(blank)") + "\n" +
      "hours: " + (entry.hours === "" || entry.hours == null ? "(blank)" : entry.hours) + "\n" +
      "activity: " + (entry.activity || "(blank)") + "\n\n" +
      "This volunteer's already-approved entries:\n" + history + "\n\n" +
      "Decide if a careful coordinator should review this before approving. Checks:\n" +
      "- impossible_hours: hours <= 0, greater than 24 for one day, or impossible.\n" +
      "- missing_field: name, date, or hours blank/unreadable.\n" +
      "- vague_activity: activity blank or uninformative (\"stuff\", \"things\", \"helped out\").\n" +
      "- activity_mismatch: hours grossly inconsistent with the activity (e.g. 20h to send one email).\n" +
      "- duplicate: same date and activity as one of the approved entries above.\n\n" +
      "Return this JSON shape only:\n" +
      '{"status":"ok"|"review","flags":[<zero or more of: duplicate, impossible_hours, missing_field, activity_mismatch, vague_activity>],"note":"<one short plain sentence for a coordinator; empty string if ok>"}';

    var res = await fetch("https://api.anthropic.com/v1/messages", {
      method: "POST",
      headers: {
        "content-type": "application/json",
        "x-api-key": state.apiKey,
        "anthropic-version": "2023-06-01",
        "anthropic-dangerous-direct-browser-access": "true"
      },
      body: JSON.stringify({
        model: state.model,
        max_tokens: 400,
        system: system,
        messages: [{ role: "user", content: user }]
      })
    });
    if (!res.ok) {
      var t = await res.text().catch(function () { return ""; });
      throw new Error("API " + res.status + (t ? ": " + t.slice(0, 160) : ""));
    }
    var data = await res.json();
    var text = (data.content || []).map(function (b) { return b.type === "text" ? b.text : ""; }).join("");
    var cleaned = text.replace(/```json/g, "").replace(/```/g, "").trim();
    var parsed = JSON.parse(cleaned);
    return {
      status: parsed.status === "review" ? "review" : "ok",
      flags: Array.isArray(parsed.flags) ? parsed.flags : [],
      note: parsed.note || ""
    };
  }

  // ---- views (return HTML strings) -----------------------------------------
  function tagHtml(flags) {
    return '<div class="tags">' + flags.map(function (f) {
      return '<span class="tag">' + esc(FLAG_LABELS[f] || f) + "</span>";
    }).join("") + "</div>";
  }

  function submitView() {
    var m = state.submitMsg, msgHtml = "";
    if (m && m.error) {
      msgHtml = '<div class="error">' + esc(m.error) + "</div>";
    } else if (m) {
      msgHtml =
        '<div class="result ' + m.verdict + '">' +
          "<h4>" + (m.verdict === "ok" ? "Looks clean — sent for approval" :
            "Sent for approval, but flagged for a closer look") + "</h4>" +
          (m.flags.length ? tagHtml(m.flags) : "") +
          (m.note ? "<p>" + esc(m.note) + "</p>" : "") +
        "</div>";
    }
    return (
      '<p class="lede-sm">Log the hours you worked. Each entry is checked, then held for a coordinator ' +
      "to approve — approved hours roll into your running total automatically.</p>" +
      '<div class="form-grid">' +
        field("Your name", "f-name", "Maria Gonzalez") +
        field("Date", "f-date", "2025-06-03") +
        field("Hours", "f-hours", "3") +
        field("Activity", "f-activity", "Phone banking, ~40 calls") +
      "</div>" +
      '<button class="btn" id="submit-btn">Submit hours</button>' +
      msgHtml
    );
  }
  function field(label, elId, ph) {
    return '<div class="field"><label>' + label + '</label>' +
      '<input id="' + elId + '" placeholder="' + esc(ph) + '" /></div>';
  }

  function reviewView() {
    if (!state.pending.length) {
      return empty("Nothing waiting", "Submitted hours land here for approval. The queue is clear.");
    }
    var items = state.pending.map(function (e) {
      var flagged = e.verdict === "review";
      var note = e.note ? '<div class="qi-note ' + e.verdict + '">' + esc(e.note) + "</div>"
        : (!flagged ? '<div class="qi-note ok">No issues found.</div>' : "");
      return (
        '<div class="queue-item ' + e.verdict + '">' +
          '<div style="flex:1">' +
            '<div class="qi-name">' + esc(e.name) +
              '<span class="qi-meta">' + esc(e.date) + " · " + esc(e.hours) + "h</span></div>" +
            '<div class="qi-activity">' + esc(e.activity) + "</div>" +
            (flagged && e.flags.length ? tagHtml(e.flags) : "") +
            note +
          "</div>" +
          '<div class="qi-actions">' +
            '<button class="btn btn-verified" data-approve="' + e.id + '">Approve</button>' +
            '<button class="btn btn-ghost btn-flag" data-reject="' + e.id + '">Reject</button>' +
          "</div>" +
        "</div>"
      );
    }).join("");
    return (
      '<p class="lede-sm">Every submission waits here until you decide. The check is advice, not a gate — ' +
      "you can approve a flagged entry or reject a clean one.</p>" + items
    );
  }

  function ledgerView() {
    if (!state.approved.length) {
      return empty("No approved hours yet",
        "Once a coordinator approves an entry, it's recorded here and counts toward that volunteer's total — and it stays in this browser between visits.");
    }
    var byPerson = {};
    state.approved.forEach(function (e) {
      if (!byPerson[e.name]) byPerson[e.name] = { hours: 0, count: 0 };
      byPerson[e.name].hours += Number(e.hours) || 0;
      byPerson[e.name].count += 1;
    });
    var people = Object.keys(byPerson).map(function (n) {
      return { name: n, hours: byPerson[n].hours, count: byPerson[n].count };
    }).sort(function (a, b) { return b.hours - a.hours; });
    var grand = state.approved.reduce(function (s, e) { return s + (Number(e.hours) || 0); }, 0);

    var rows = people.map(function (p) {
      return "<tr><td class='name'>" + esc(p.name) + "</td>" +
        "<td class='num count'>" + p.count + "</td>" +
        "<td class='num hrs'>" + p.hours.toFixed(1) + "</td></tr>";
    }).join("");

    var entries = state.approved.slice().reverse().map(function (e) {
      return '<div class="entry-row">' +
        '<span class="er-name">' + esc(e.name) + "</span>" +
        '<span class="er-date">' + esc(e.date) + "</span>" +
        '<span class="er-hrs">' + esc(e.hours) + "h</span>" +
        '<span class="er-act">' + esc(e.activity) + "</span></div>";
    }).join("");

    return (
      '<div class="summary"><div class="big">' + grand.toFixed(1) + "</div>" +
      '<div class="lbl">total approved hours across ' + people.length +
        " volunteer" + (people.length === 1 ? "" : "s") + "</div></div>" +
      '<div class="section-label">Running totals<span></span></div>' +
      '<div class="tbl-wrap"><table><thead><tr><th>Volunteer</th>' +
        "<th class='num'>Entries</th><th class='num'>Approved hours</th></tr></thead>" +
        "<tbody>" + rows + "</tbody></table></div>" +
      '<div class="section-label">Approved entries<span></span></div>' +
      '<div class="entries">' + entries + "</div>"
    );
  }

  function empty(title, body) {
    return '<div class="empty"><h3>' + esc(title) + "</h3><p>" + esc(body) + "</p></div>";
  }

  function settingsRow() {
    var ok = state.apiKey
      ? '<span class="keyok">key saved ✓</span>' : "";
    return (
      '<div class="settings">' +
        '<div class="grow"><label>Anthropic API key (stays in this browser)</label>' +
          '<input id="s-key" type="password" placeholder="sk-ant-..." value="' + esc(state.apiKey) + '" /></div>' +
        '<div style="min-width:170px"><label>Model</label>' +
          '<input id="s-model" value="' + esc(state.model) + '" /></div>' +
        '<button class="btn" id="save-settings">Save</button>' +
        (ok ? '<div style="align-self:center">' + ok + "</div>" : "") +
      "</div>" +
      '<p class="hint">Get a key at <a href="https://console.anthropic.com/settings/keys" target="_blank" rel="noreferrer">console.anthropic.com</a>. ' +
      "It's stored only in your browser and sent directly to Anthropic. Never commit your key to the repo. " +
      "Confirm the model name at <a href='https://docs.claude.com/en/docs/about-claude/models' target='_blank' rel='noreferrer'>the models page</a>.</p>"
    );
  }

  // ---- render --------------------------------------------------------------
  function render() {
    var tabs = [["submit", "Submit hours"], ["review", "Review queue" + (state.pending.length ? " · " + state.pending.length : "")], ["ledger", "Approved ledger"]];
    var body = state.tab === "submit" ? submitView() : state.tab === "review" ? reviewView() : ledgerView();

    document.getElementById("app").innerHTML =
      '<div class="wrap">' +
        '<div class="eyebrow">self-service · runs in the background</div>' +
        "<h1>Volunteer-Hours Ledger</h1>" +
        '<p class="lede">Volunteers log their own hours, each entry is checked and sent for approval, ' +
          "and approved time keeps a running per-person total.</p>" +
        settingsRow() +
        '<div class="tabs">' + tabs.map(function (t) {
          return '<button class="tab ' + (state.tab === t[0] ? "active" : "") + '" data-tab="' + t[0] + '">' + esc(t[1]) + "</button>";
        }).join("") + "</div>" +
        body +
        '<div class="footer">Entry checks performed by Claude, called directly from your browser with your key · ' +
          "approved hours saved in this browser (localStorage) · demo project — use sample data only</div>" +
      "</div>";
    bind();
  }

  // ---- event binding -------------------------------------------------------
  function bind() {
    document.querySelectorAll("[data-tab]").forEach(function (b) {
      b.onclick = function () { state.tab = b.getAttribute("data-tab"); state.submitMsg = null; render(); };
    });
    var saveBtn = document.getElementById("save-settings");
    if (saveBtn) saveBtn.onclick = function () {
      state.apiKey = (document.getElementById("s-key").value || "").trim();
      state.model = (document.getElementById("s-model").value || "claude-sonnet-5").trim();
      localStorage.setItem(K.key, state.apiKey);
      localStorage.setItem(K.model, state.model);
      render();
    };

    var submitBtn = document.getElementById("submit-btn");
    if (submitBtn) submitBtn.onclick = onSubmit;

    document.querySelectorAll("[data-approve]").forEach(function (b) {
      b.onclick = function () { onApprove(b.getAttribute("data-approve"), b); };
    });
    document.querySelectorAll("[data-reject]").forEach(function (b) {
      b.onclick = function () { onReject(b.getAttribute("data-reject")); };
    });
  }

  // ---- actions -------------------------------------------------------------
  async function onSubmit() {
    var entry = {
      name: (document.getElementById("f-name").value || "").trim(),
      date: (document.getElementById("f-date").value || "").trim(),
      hours: document.getElementById("f-hours").value,
      activity: (document.getElementById("f-activity").value || "").trim()
    };
    if (!state.apiKey) { state.submitMsg = { error: "Add your Anthropic API key above first." }; render(); return; }
    if (!entry.name || !entry.date || entry.hours === "" || !entry.activity) {
      state.submitMsg = { error: "Fill in every field — the check needs all four to be useful." }; render(); return;
    }
    entry.hours = Number(entry.hours);

    var btn = document.getElementById("submit-btn");
    btn.disabled = true; btn.textContent = "Checking…";
    try {
      var verdict = await checkEntry(entry);
      var record = {
        id: id(), name: entry.name, date: entry.date, hours: entry.hours, activity: entry.activity,
        verdict: verdict.status, flags: verdict.flags, note: verdict.note, submittedAt: new Date().toISOString()
      };
      state.pending.push(record);
      save(K.pending, state.pending);
      state.submitMsg = { verdict: verdict.status, flags: verdict.flags, note: verdict.note };
    } catch (e) {
      state.submitMsg = { error: "Couldn't run the check. " + (e.message || "Try again.") };
    }
    render();
  }

  function onApprove(entryId, btn) {
    if (btn) { btn.disabled = true; btn.textContent = "…"; }
    var entry = state.pending.filter(function (p) { return p.id === entryId; })[0];
    if (!entry) return;
    state.pending = state.pending.filter(function (p) { return p.id !== entryId; });
    entry.approvedAt = new Date().toISOString();
    state.approved.push(entry);
    save(K.pending, state.pending); save(K.approved, state.approved);
    render();
  }

  function onReject(entryId) {
    state.pending = state.pending.filter(function (p) { return p.id !== entryId; });
    save(K.pending, state.pending);
    render();
  }

  render();
})();
</script>
</body>
</html>
