## Public chatbot url 
> https://cloud.flowiseai.com/chatbot/2c9f31ba-43dc-4175-907a-9f519584fb95

## Github link 
> https://github.com/deepchika-bhutia/scm-assistant-bot

## LLM 
> gemini-2.5-flash and gemini-2.5-flash-lite

## embedding 
> gemini-embedding-001

## chunk configs tried : 
1. size : 2000 and overlap : 250  recursive charecter text splitter -- produces 12 chunks but the chunks are not divided according to sections and subsections of the text
2. used Markdown Text Splitter to split by H2 to give 11 chuncks 1 for introduction and 10 sections from the table of contents. one chunk is information dense in regards to a particular section, making retrieval efficient multiple chunks dont need to be called for a single section

## Questions
1. 
    Q1. Which Tier-3 suppliers have an active disruption flag, and what response level applies per policy?

    A1. The following Tier-3 suppliers have an active disruption flag:

    Level 3 (Activate) Response (per Policy §9, for High Risk suppliers):

    Maghreb Castworks
    Deltaforge Vietnam
    Dravex Components India
    Buenos Aires Pack
    Orinoco Pack SAPI
    Sibertek Molding
    Archipelago PCB Corp
    Patagonia Alloys SRL
    Visayas Textile Co
    Plataforma Metales SA
    DaNang Metal Works
    Varna Electronics EAD
    Bohai Electronics
    Longhua Polymer Works
    Bogota Pack Ltda
    Lima Polymer SA
    Sahyadri Alloy Tech
    Quetzal Textiles
    Vistula Pack Sp
    Yucatan Polymer Mfg
    Cerromax Mineria
    Deccan Polymer Mfg
    MeKong Pack Co
    Level 2 (Manage) Response (per Policy §9, for Medium Risk suppliers):

    Helios Pack Greece
    Per Policy §9, the disruption response levels are:

    Level 3 (Activate): Requires immediate escalation to the CPO, activation of alternate suppliers for a minimum of 40% of volume within 10 business days, a +50% safety stock adjustment, and a full root cause analysis (RCA) within 15 business days.
    Level 2 (Manage): Requires bi-weekly escalation calls, a +30% safety stock adjustment, and alternate suppliers on 48-hour readiness notice.
---
2. 
    Q2. Which suppliers qualify for the annual Volume Rebate Program and how many are there?

    A2. No suppliers qualify for the annual Volume Rebate Program.

    Per Policy §4.2, Tier-1 suppliers with all of the following for a full calendar year qualify for an annual volume rebate of 2.5% of total annual invoice value:

    OTD at or above 93.0%
    Defect Rate below 0.5%
    Sustainability Score at or above 85

---
3. 
    Q3. Which region has the highest total PO value, and does it breach the concentration limit?

    A3. The APAC region has the highest total PO value of $131,620,356.14.

    Per Policy §5.3, no single region may account for more than 45% of total annual procurement spend. The total annual procurement spend is $356,045,248.18.

    The APAC region accounts for approximately 36.96% of the total annual procurement spend ($131,620,356.14 / $356,045,248.18 * 100). Therefore, it does not breach the concentration limit.

---
4. 
    Q4. Which suppliers are on Supplier Watch List (SWL) status and what does it restrict?

    A4. The following suppliers are on Supplier Watch List (SWL) status because their compliance score is below 60: Bohai Electronics, Deccan Polymer Mfg, Longhua Polymer Works, Sibertek Molding, Buenos Aires Pack, Visayas Textile Co, DaNang Metal Works, Sahyadri Alloy Tech, Dravex Components India, Patagonia Alloys SRL, Plataforma Metales SA, Bogota Pack Ltda, Yucatan Polymer Mfg, Maghreb Castworks, Helios Pack Greece, Deltaforge Vietnam, MeKong Pack Co, Varna Electronics EAD, Lima Polymer SA, Cerromax Mineria, Archipelago PCB Corp, Vistula Pack Sp, Quetzal Textiles, and Orinoco Pack SAPI.

    Per Policy §3.4, SWL status restricts new PO issuance to 20% of the prior quarter's volume.

---
5. 
    Q5. Which product category has the highest average defect rate and does it exceed the Tier-2 limit?

    A5. The product category with the highest average defect rate is 'Packaging Materials' with an average defect rate of 1.909%.

    Per Policy §3.2, the maximum permissible defect rate for Tier-2 suppliers is 2.50%. Since 1.909% is below 2.50%, it does not exceed the Tier-2 limit.


## Future Improvements

- smaller embeddings, for lower token usage
- non linear embedding connections, like when a section refers to another section that is not adjacent to it 
- add a caching mechanism for sql queries on top of caching LLM responses
