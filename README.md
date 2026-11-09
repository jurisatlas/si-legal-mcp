# Slovenia Legal Research MCP Server (`si-legal-mcp`)

**[Slovenščina](#lang-sl) | [English Documentation](#english-documentation)**

---

<a id="lang-sl"></a>
## Pravni MCP Strežnik za Republiko Slovenijo (`si-legal-mcp`) — Slovenščina

### O tem repozitoriju

Ta repozitorij vsebuje MCP strežnik za povezavo vašega AI pomočnika (Claude Desktop, Cursor, Windsurf, VS Code, Antigravity) s Pravno-informacijskim sistemom RS (`pisrs.si`) in bazo Sodna praksa (`sodnapraksa.si`), ki vključuje okrajna in okrožna sodišča, 4 višja sodišča (Ljubljana, Maribor, Celje, Koper), Upravno sodišče, Vrhovno sodišče RS in Ustavno sodišče RS.

### Hitra namestitev (Izbira AI programa)

1. **Prenos:** Kliknite **`<> Code` -> `Download ZIP`** in razširite mapo na računalniku.
2. **Zagon:** Dvokliknite **`Click_Here_To_Install_Windows.bat`** (Windows) ali **`Click_Here_To_Install_Mac.command`** (macOS).
3. **Izbira AI odjemalca:** Označite AI programe, ki jih uporabljate, kliknite na namestitev in ponovno zaženite izbrano AI aplikacijo.

**Varnostno opozorilo:** Namestitveni program deluje izključno v bralnem načinu (read-only) in ne dostopa do vaših osebnih datotek.

### Stopnje sodišč in uradni viri

| Stopnja sodišča | Zajeta sodišča |
|:---|:---|
| **1. stopnja (Okrajna in okrožna sodišča)** | Okrajna sodišča (44 Local Courts), Okrožna sodišča (11 District Courts), Delovna sodišča & Upravno sodišče RS |
| **2. stopnja (4 Višja sodišča)** | 4 Višja sodišča (Ljubljana, Maribor, Celje, Koper) & Višje delovno in socialno sodišče |
| **3. stopnja (Vrhovno in Ustavno sodišče RS)** | Vrhovno sodišče Republike Slovenije (VSRS) & Ustavno sodišče Republike Slovenije (USRS) |

- **PISRS - Pravno-informacijski sistem Republike Slovenije (pisrs.si):** [https://pisrs.si](https://pisrs.si) (`pisrs.si`, `uradni-list.si`, `dz-rs.si`)
- **Sodna praksa RS (sodnapraksa.si — Višja sodišča, Upravno sodišče & Vrhovno sodišče):** [https://www.sodnapraksa.si](https://www.sodnapraksa.si) (`sodnapraksa.si`, `sodisce.si`, `us-rs.si`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Slovenia (SI)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Slovenia**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | Okrajna sodišča (44 Local Courts), Okrožna sodišča (11 District Courts), Delovna sodišča & Upravno sodišče RS |
| **Tier 2 — Regional / Cantonal / Appellate** | 4 Višja sodišča (Ljubljana, Maribor, Celje, Koper) & Višje delovno in socialno sodišče |
| **Tier 3 — Supreme & Constitutional** | Vrhovno sodišče Republike Slovenije (VSRS) & Ustavno sodišče Republike Slovenije (USRS) |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** PISRS - Pravno-informacijski sistem Republike Slovenije (pisrs.si) — [https://pisrs.si](https://pisrs.si)
  - *Indexed Legislation Domains:* `pisrs.si`, `uradni-list.si`, `dz-rs.si`
- **Court Decisions & Jurisprudence Archives:** Sodna praksa RS (sodnapraksa.si — Višja sodišča, Upravno sodišče & Vrhovno sodišče) — [https://www.sodnapraksa.si](https://www.sodnapraksa.si)
  - *Indexed Judicial & Open Case Law Domains:* `sodnapraksa.si`, `sodisce.si`, `us-rs.si`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Slovenia. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Slovenia. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Slovenia. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "si-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/si-legal-mcp/archive/refs/heads/main.zip",
        "si-legal-mcp"
      ]
    }
  }
}
```
</details>
