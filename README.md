# Soumya Sethy

Software architect & 0→1 product builder. Building AI-on-ERPNext — **LazyChat** (101-tool MCP server, open source) and **LazyCode** (AI coding agent for Frappe, private beta). Previously architected and shipped a Shopify-class omnichannel e-commerce stack end-to-end on ERPNext for a fashion D2C brand, from manufacturing through last-mile delivery, on one ledger.

Bangalore. Shipping in the open since 2013.

[LinkedIn](https://linkedin.com/in/soumyasethy) · [Medium](https://medium.com/@soumyasethy) · [X](https://x.com/soumyarsethy)

---

## Now

I'm building [**lazychat-erpnext**](https://github.com/soumyasethy/lazychat-erpnext), an open-source AI assistant docked into the ERPNext desk. It's a 101-tool MCP server with bring-your-own LLM — any OpenAI-compatible or Anthropic key, the key stays in your browser. Mutations are Apply-gated; a vision-judge loop drives self-iteration. The Frappe community's first AI-native sidekick.

Alongside it, **LazyCode.in** (private beta) — an AI coding agent for Frappe and ERPNext apps. LazyChat helps users *work* in ERPNext. LazyCode helps developers *build* on it.

---

## Production

I architected and built a Shopify-class omnichannel e-commerce stack from zero for a fashion D2C brand — manufacturing to last-mile, reconciled to one ledger. Today, multiple ERPNext companies run on the same Frappe backbone in production. I own the end-to-end process design across **P2P** (Procure-to-Pay), **O2C** (Order-to-Cash), and **R2R** (Record-to-Report), and I designed and shipped the functional systems behind them: OMS, WMS, PIM, PLM, MES, marketplace listing and inventory sync, and product traceability with EAN and serialization.

The architecture separates Master Data, Transactions, and Financial R2R into three layers; B2B, D2C, and marketplace channels reconcile to one ledger. Forward and return flows include serial-number FIFO matching, `isReturn` invoice flagging, and automatic credit/debit notes. The webhook surface covers GRN inbound, the outward order lifecycle — create, complete, shipment-dispatch, deliver, cancel, partial-cancel — and channel returns. A Shopify D2C webhook stream handles order and customer events.

<p align="center">
  <img src=".github/assets/erp-architecture.svg" alt="ERP architecture — Master Data, Transactions, R2R" width="100%"/>
</p>

Live integrations run through a Java-based middleware platform I architected — connectors, retry, idempotency, audit trail — sitting between ERPNext and the operating world. It wires ERPNext to **e-Waybill** (Indian goods-movement compliance), **Shiprocket + Cargofl** (last-mile delivery aggregators), **GSTR-1** (statutory returns automation), **EAN barcoding** for traceability and serialization, and **five-bank H2H banking** — ICICI, HDFC, AXIS, YES, Kotak Mahindra — via [india-banking](https://github.com/agi-engg/india-banking) on Frappe. On the D2C ecosystem side, integrations include **Shopify Plus**, **Gokwik** (one-click checkout), and **Return Prime** (returns management). Full-ecosystem fluency with **Increff** covers WMS, OMS, CIMS, ICC, reports, and tech operations.

Stack: React + TypeScript + Tailwind + Vite + Storybook for the storefront; React Native and Flutter for companion mobile apps; Frappe/ERPNext (Python) with Java microservices, Node BFFs, and Kafka on the backend; PostgreSQL, MariaDB, Redis, and BigQuery for data; GCP, Docker, GitHub Actions, and Cloudflare for infrastructure.

---

## Behind the wall

The open-source pieces above are a slice. Behind the [@agi-engg](https://github.com/agi-engg) wall sit roughly fifty private services and apps I've architected and led: AI pricing-intelligence (ML-driven SKU pricing), AI customer chatbots, a Customer Data Platform (Java + Kafka + BigQuery, with a 360° view across web, app, marketplace and OMS), WMS extensions on top of Increff (bulk-picking, put-away), a 3D tech-pack tool for fashion design-to-BOM, warranty and return workflow apps on ERPNext, API gateways with unified auth, rate-limit and observability, shop-floor mobile apps for MES, an internal control-center dashboard that's the team's single pane of glass, and the corporate web properties — careers, policy portal, brand sites.

---

## Journey

Started on Android in 2013, with CS algorithm work that produced a Splitwise CashFlow implementation (15★). Through 2017–2020, the mobile era — React Native from scratch, Flutter clones (Inshorts, 8★). From 2020 to 2023, frontend platforms: widgetized JSON UIs, micro-frontends, design systems at Figma-class scope. From 2023 to 2025, the Shopify-class e-commerce build on ERPNext, with Java middleware live across e-Waybill, Shiprocket + Cargofl, GSTR-1, Increff, and five banks; multi-company in production. From 2025 onward, AI-on-ERPNext — LazyChat (101-tool MCP, BYO LLM) and LazyCode.

---

## Talk

If you run an ERPNext shop and want AI on top, start with [lazychat-erpnext](https://github.com/soumyasethy/lazychat-erpnext).

If you're building a 0→1 product and need a software architect or technical co-founder, [LinkedIn](https://linkedin.com/in/soumyasethy) or [DMs open on X](https://x.com/soumyarsethy).
