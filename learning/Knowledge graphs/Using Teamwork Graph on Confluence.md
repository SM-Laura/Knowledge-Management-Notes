## 1. Understand what “using Teamwork Graph” means

From Atlassian’s documentation:

> “Teamwork Graph unifies and connects data about **teams, projects, goals, and third-party apps** across your Atlassian ecosystem. The graph establishes a **unified data model** that acts as a **foundational layer** for platform experiences like **Rovo, search, agents, analytics, and automation**.”  
> [Connect Workday to your Teamwork Graph | Atlassian Support](https://support.atlassian.com/organization-administration/docs/add-connector-for-workday/)

So you don’t “turn on” Teamwork Graph as a product; you use it in two ways:

1. **As an end user** via features powered by it (Rovo, AI, search, Studio, etc.).
    
2. **As an admin / builder / developer** by connecting more systems and/or building against the graph.
    

---

## 2. As an end user: you’re already using it via Rovo & Studio

Teamwork Graph is already the data layer for:

1. **Rovo Chat, Search, and Agents**  
    Your own Confluence page describes this:
    
    _“Rovo uses Atlassian’s proprietary Teamwork Graph—a unified data model connecting information across your organization’s tools.”_  
    [Maximizing Productivity with Rovo: Your AI-Powered Atlassian Teammate](https://keyloop.atlassian.net/wiki/spaces/CIDT/pages/911114373/Maximizing+Productivity+with+Rovo+Your+AI-Powered+Atlassian+Teammate)
    
    Any time you:
    
    - Ask Rovo Chat questions that span people / pages / Jira work
        
    - Use Rovo Search to find “pages linked to epic KEY‑123”
        
    - Interact with Rovo Agents that summarize or act across tools
        
    
    …you’re already consuming Teamwork Graph.
    
2. **Rovo Studio (if enabled for your org)**
    
    Rovo Studio is explicitly described as building on Teamwork Graph:
    
    _“Rovo Studio uses Rovo AI and your organization’s **Teamwork Graph** (the data that connects people, work, and content in Atlassian Cloud) so the solutions you build can act with context about your projects, spaces, coworkers, and customers…”_  
    [What is Rovo Studio? | Rovo Studio | Atlassian Support](https://support.atlassian.com/studio/docs/what-is-rovo-studio/)
    
    To “start using” it here:
    
    - Open **Rovo Studio** from the Atlassian app switcher.
        
    - Use Rovo Chat _inside_ Studio with prompts like:
        
        - “Create an agent that answers PS consultants’ questions using our Confluence PS KB.”
            
        - “Create an automation that pings the owner when a MIC page hasn’t been updated in 6 months.”
            
    
    Behind the scenes, Studio uses Teamwork Graph to know:
    
    - Who people are, which teams they’re in
        
    - What work items / pages relate to which projects, etc.
        

So: as a PS / KM practitioner, you “start using Teamwork Graph” by leaning into these features and asking cross‑tool, relationship‑heavy questions in Rovo.



## **What you can (and can’t) do with “cross-tool connections” today**

With **out-of-the-box Rovo connectors** (e.g., SharePoint/OneDrive, Miro), you generally **can’t manually create a first-class “Space X ↔ SharePoint Site Y” edge** in Teamwork Graph via a UI.

What you _can_ do is:

1. **Ensure the external items are actually ingested & permission-visible** to Rovo (connector + per-user auth).
    
2. **Create strong canonical-ish signals** that Rovo/Graph can follow: _explicit links (Smart Links), curated “index pages”, consistent IDs/names, backlinks_.
    
3. If you truly need deterministic graph edges: **create relationships at ingestion time** (custom connector / EAP) using Teamwork Graph relationship mechanics.
    

---

## **A) Make sure Rovo can “see” the SharePoint/Miro content at all**

### **1) Connector installed + indexing scope is correct**

- **Miro**: the connector **only connects to a single Miro team** (so boards outside that team won’t be in Rovo).  
    Docs: [Connect Miro to Rovo | Atlassian Support](https://support.atlassian.com/organization-administration/docs/connect-miro-to-rovo/)
    
- **SharePoint/OneDrive**: Rovo indexes the workspace and can be **scoped down via blocklist** for some connectors (incl. SharePoint).  
    Docs: [Teamwork Graph data, privacy, and usage guidelines | Atlassian Support](https://support.atlassian.com/organization-administration/docs/teamwork-graph-data-privacy-and-usage-guidelines/)
    

### **2) Users must be able to authenticate (permission-aware)**

Even if the connector is admin-managed, users may be prompted to **connect their account** so Rovo can respect their existing permissions.  
Docs: [How Rovo connector permissions are kept in sync | Atlassian Support](https://support.atlassian.com/organization-administration/docs/how-connector-permissions-are-kept-in-sync/)

### **3) Quick validation**

Use **Rovo Search** and filter by the app (SharePoint / Miro) to confirm items are indexed and visible to you. (If you can’t find it in Search, Chat/Agents also typically won’t reliably use it.)

---

## **B) How to “connect” a Confluence space/page to SharePoint docs or Miro boards (without custom development)**

### **1) Create explicit links using Smart Links (the most practical lever)**

On the relevant Confluence pages (often the **space homepage**, a “Start here” page, or a **hub/index page**):

- Paste the **SharePoint document / folder URL** and keep it as a **Smart Link card/embed**
    
- Paste the **Miro board URL** and keep it as a **Smart Link card/embed**
    
- Add a dedicated section like **“Authoritative sources / Source of truth”** with those links
    

Why this helps:

- It creates **explicit cross-tool references** that Rovo can retrieve as context.
    
- Smart Links can also become searchable in Rovo (depending on connector type).
    

Smart Links + search behavior details:

- Searchable Smart Links list includes **Miro boards** and **SharePoint docs**.  
    Docs: [Search with Smart Links | Rovo | Atlassian Support](https://support.atlassian.com/rovo/docs/search-with-smart-links/)
    
- Smart Link basics: [Smart Links from across Atlassian and other apps | Platform experiences | Atlassian Support](https://support.atlassian.com/platform-experiences/docs/smart-links-from-jira-and-other-products/)
    

**Important nuance:** searchable Smart Links in Rovo Search only appear if the Smart Link is on a page **you’ve viewed** (per the docs). That’s still useful for “making the connection real” in day-to-day work, but it’s not a perfect org-wide mapping mechanism.

### **2) Build a Confluence “mirror index” pattern (best practice for KM)**

If you want a durable, maintainable relationship between a Confluence space and a SharePoint site/library or a set of Miro boards:

- Create a Confluence page like:  
    `Space Hub → External Knowledge Index`
    
- Put:
    
    - A Smart Link to the **SharePoint site/library**
        
    - A curated list of the **top 10–30 key SharePoint docs** (Smart Links)
        
    - A curated list of the **canonical Miro boards** (Smart Links)
        
    - A short “when to use Confluence vs SharePoint vs Miro” note
        

This gives Rovo a _single, high-signal anchor page_ that naturally bridges systems.

### **3) Add backlinks from SharePoint/Miro back to Confluence**

Where possible:

- In **SharePoint docs**, add a “Related Confluence page” link back to the hub page.
    
- In **Miro board description**, add the Confluence hub link.
    

This improves retrieval because the same pairing is expressed in both places (and is also helpful for humans).

---

## **C) Ensure Rovo Chat / Agents “keep those sources in mind”**

### **1) Rovo Chat (ad hoc)**

If SharePoint/Miro is connected and you have access, Rovo Chat can use that content—_but it will prioritize what’s easiest to retrieve as relevant_.

To make it consistently pull the right sources:

- Ask questions with constraints like:  
    _“Answer using our Confluence PS KB **and the linked SharePoint ‘Manuals’ library**.”_
    
- Include the hub/index page in the prompt (or ask it to start from that page).
    

### **2) Rovo Agents (repeatable, controlled)**

Agents have an explicit **Knowledge scope**:

- By default, agents can use **All organizational knowledge** (i.e., what admins connected via Teamwork Graph/Rovo).
    
- You can narrow to **Custom knowledge** (specific spaces/pages/branches, etc.).
    

Docs: [Knowledge sources for Rovo agent scenarios | Rovo | Atlassian Support](https://support.atlassian.com/rovo/docs/knowledge-sources-for-agents/)

**Practical implication for your use case:**

- If the Agent UI **doesn’t let you explicitly pick SharePoint/Miro as “custom knowledge”** (this varies by rollout), the reliable workaround is:
    
    - Put the SharePoint/Miro Smart Links on a **single Confluence hub page**, and
        
    - Add **that hub page/branch** as the agent’s Custom knowledge.
        

That way the agent is “forced” to see the curated bridge, even when operating in a narrowed scope.