---
title: Nejčastější dotazy týkající se integrace aplikace Dynamics 365 for Talent s Dynamics 365 for Finance and Operations
description: Toto téma vysvětluje, jaká data jsou synchronizována v rámci integrace aplikací Talent a Finance and Operations.
author: negudava
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aea025bc4898d6399e82030cf1f52b21949e014f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303609"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>Nejčastější dotazy týkající se integrace aplikace Dynamics 365 for Talent s Dynamics 365 for Finance and Operations

[!include [banner](includes/banner.md)]

Toto téma uvádí odpovědi na časté otázky spojené s tím, jaká data jsou synchronizována při integraci aplikace Dynamics 365 for Talent s Dynamics 365 for Finance and Operations.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Jsou synchronizovaná všechna data nebo jenom některé datové entity?

S aplikací Core Human Resources (HR) je synchronizována dílčí skupina dat. Seznam všech entit uvádí téma [Integrace z aplikace Dynamics 365 for Talent do Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).

V případě Attract a Onboard jsou všechna data nativní pro Common Data Service (CDS) pro aplikace.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Je možné vytvořit nové mapování bez použití šablon

Šablony jsou počátečním bodem. Můžete vytvořit vlastní šablonu, ale při vytváření projektu integrace je šablona potřeba vždy. Další informace o šablonách integrátoru dat (DI) a projektech naleznete v tématu [Integrace dat v Common Data Service pro aplikace](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Lze mapovat finanční dimenze k přenosu mezi aplikacemi Talent and Finance and Operations?

Finanční dimenze aktuálně nejsou v CDS pro aplikace a proto nejsou součástí výchozí šablony. Tato entita je plánována, ale v současné době není k dispozici žádná časová osa pro uvolnění.

V případě dat, která existují v modulu Finance and Operations, ale ne v aplikaci Talent, spojte tyto dva systémy pomocí příkazu **Konfigurovat odkazy** v aplikaci Talent. Další informace o tom, jak konfigurovat propojení mezi aplikacemi Talent a Finance and Operations získáte v tématu [Co je nového nebo změněného v Dynamics 365 for Talent Core HR (October 31, 2018)](whats-new-talent-october-31.md).

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>Někdy se stane, že když importuji zaměstnance, přejdou v modulu Finance and Operations mezi neaktivní zaměstnance. Proč?

Jestliže zaměstnanci nemají záznam podrobností o aktivním zaměstnání v aplikaci Talent může dojít k této chybě. Chybu vyřešíte tak, že přejdete na položky **Správa zaměstnanců \> Zaměstnanci \> Historie zaměstnání \> Správce dat** a ověříte, že existuje aktivní záznam detailů zaměstnání.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Pokud vyberu možnost mapovat pouze dílčí sadu polí, spustí provedené změny provedené v nemapovaných polích synchronizaci?

Synchronizace dat řídí plán provedení. Integrace vyzvedne záznam, pokud se změní některé pole v záznamu, bez ohledu na to, zda je pole součástí mapování integrace.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Jak se dají poslat pouze změny aktivního pracovníka a ne ukončené záznamy?

S použitím "Rozšířeného dotazu" můžete filtrovat a měnit tvar zdrojových dat před předáním do cíle.

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>Můžu určit pole, která chcete odeslat do modulu Finance and Operations pro konkrétní entitu?

Pole lze přidat nebo odebrat z úkolu integrace. Ne všechna datová pole, která existují na CDS pro aplikace (CD 2.0) budou doplněna z Core HR.
Prostřednictvím PowerApps lze naplnit další data.

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Mám nastavenou integraci jako dávkovou úlohu, ale Talent ztratil připojení do cílového systému. Jak se dá odeslat stejná sada změny do cílového systému?

Není potřeba žádné speciální nastavení pro zpracování výjimek. Integrátor dat automaticky zachytí a zaznamená chyby, které se objevují ve zdroji a cíli a umožní ruční opakování. Avšak nepovoluje ruční opravy dat. Pokud je nutné provést aktualizace dat, mělo by se tak stát ve zdroji nebo v cíli.

## <a name="can-i-set-up-bi-directional-integration"></a>Můžu nastavit integraci obousměrně?

Ne, integrace je v současné době jednosměrná (z aplikace Talent do aplikace Finance and Operations). Je však k dispozici výchozí šablona pro odeslání dat z aplikace Talent do Finance and Operations.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Můžu povolit odstranění záznamu v rámci Moje integrace?

Ne, integrátor dat nebude zaznamenávat odstraněné záznamy pro přenos dat. V současné době jsou zahrnuta pouze data vytvoření a aktualizace (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Můžu znovu spustit chybné spuštění? Odešle se v takovém případě celý soubor nebo pouze změny?

Při prvním spuštění aplikace Integrátor dat je vždy úplné spuštění. Dalším spuštění jsou založeny na sledování změn. Při chybě spuštění se záznamy v rozsahu spuštění extrahují a odešlou z CDS poslední změny.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Při ukládání projektu se zobrazila chybová zpráva: "Projekt obsahuje chyby mapování". Co udělat?

Zkontrolujte nastavení klíčů integrace, proveďte požadované změny nastavení a aktualizujte entity v projektu.

Při použití výchozí šablony budou integrační klíče automaticky importovány. K tomuto problému může dojít, když jsou do existující šablony přidány nové úkoly.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Pokud mám nekonečný počet právnických osob, kde mají zaměstnanci zaměstnání, je nutné vytvořit mapování pro každý z nich?

Ano, pro každou právnickou osobu v modulu Finance and Operations je nutný samostatný integrační projekt v integraci dat.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Je třeba převést data, která nejsou součástí výchozí šablony od společnosti Microsoft. Lze to provést?

Ano, pole můžete přidat do existující šablony nebo z ní odebrat. Šablony lze upravit tak, aby obsahovaly další data z jiných entit aplikací CDS. Entita musí být v CDS pro aplikace, aby byla zahrnuta do šablony. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Právě jsem vytvořil nová prostředí Finance and Operations a Talent a zobrazuje se chyba Hodnota data porušuje omezení integrity. Proč?

Důvody této chyby mohou zahrnovat:

- Převod dat měl za následek extrahování duplicitních záznamů ve zdroji (CD).

- Přenos dat má hodnoty null pro pole, která jsou v aplikaci Finance and Operations povinná. Ověřte data, která se jsou v CDS a splňují požadavky modulu Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Pokud došlo k chybám provedení a neproběhla synchronizace ID zaměstnance, jak lze najít úlohu historie s neúspěšným záznamem zaměstnance?

Integrátor dat v modulu Finance and Operations vytvoří více projektů. Vztah mezi úlohou integrátoru dat a projektem Finance and Operations je jedna ku jedné.

Sledujte čas od historie provedení integrátoru dat a hledejte projekt index - 1 v modulu Finance and Operations. Pokud je číslo úlohy v integrátoru dat 9, index modulu operace Finance and Operations je 8.

1. Zaznamenejte index úkolů z integrátoru dat (v tomto případě je to "9").

![Zaznamenání indexu úkolů z integrátoru dat](media/CaptureTaskIndex.png)

2. Sledujte čas provádění projektu.

![Sledování času provádění projektu.](media/CaptureTimeOfExecution.png)

3. V aplikaci Finance and Operations vyhledejte index -1. V tomto příkladu projekt bude mít příponu 8 a čas provedení projektu indexu 0 odpovídá času provedení v kroku 2.

![Identifikace indexu](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Po integraci aplikací Talent a Finance and Operations nevidím data Talent v aplikaci Finance and Operations. Co udělat?

Integrace s aplikací Finance and Operations je proces ve dvou krocích. Nejprve ověřte, že jsou data aplikace Talent aktualizovaná a dostupná v CDS. To je synchronizace v reálném čase a lze ji ověřit v PowerApps pohledem na data v rámci datových entit.

![Data v CDS](media/DataInCDS.png)

Pokud se data v CDS nezobrazují požadovaným způsobem, ověřte, že je entita v integraci podporovaná. Pokud chcete zahrnout do CDS další data, bude požadována změna na straně společnosti Microsoft.

Pokud je entita podporovaná a data jsou v CDS k dispozici, ověřte, zda je v integrátoru dat správné mapování. Pokud se mapování integrátoru zdá v pořádně, ověřte, zda jsou úspěšně spuštěné úlohy správy dat. Během zpracování dávkových úloh může dojít k chybám. Další informace o způsobu použití nástroje pro správu dat naleznete v tématu [Správa dat](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>Údaje o adrese mých zaměstnanců nejdou po importu do aplikace Finance and Operations správné. Co mám dělat?

Číselná řada pro **ID skladového místa** používá stejný vzorec v aplikacích Talent i Finance and Operations. Číselné řady musí být jedinečný na obou stranách tak, aby nebyla žádná kolize adres při integraci dat z CDS do Finance and Operations.

Při implementaci aplikace Talent ověřte, zda číselné řady v aplikaci Talent a Finance and Operations nejsou stejné. Ověřte, zda nejsou všechny číselné řady stejné, když lze udržovat data v obou systémech.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Při vytvoření sady připojení nevidím připojení v rozevíracím seznamu připojení. Co udělat?

Při vytváření připojení zvolte Dynamics 365 for Finance and Operations (aktuálně v náhledu) a Common Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Při synchronizaci zaměstnání se zobrazují chyby "CompanyInfo_FK neexistuje" nebo "Hodnota 31/12 a 2154 23:59:59: 00 ' v poli Koncové datum zaměstnání nebyla nalezena v související tabulce"Zaměstnání"." Co mám dělat?

Mapujte na správné právnické osoby. Synchronizace právnické osoby není součástí výchozí šablony, takže se očekává, že každá právnická osoba přítomná v aplikacích Talent a CDS je dostupná také v aplikaci Finance and Operations.
Dále také vyberte správné právnické osoby pro přidruženou sadu připojení.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>Po nastavení projektu se zdá mapování polí pro Finance and Operations prázdné. Co mám dělat?

Aktualizujte entity dat v aplikaci Finance and Operations v části **Správa dat \> Parametry systému \> Nastavení entity \> Aktualizovat seznam entit.** Mělo by to trvat několik minut a poté by se mělo zobrazit toto mapování. K tomuto problému dochází při vytváření nových projektů.

![Mapování chybějících polí](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Další prostředky

- Integrátor dat (Di): 

  - [Integrace dat do Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [Správa chyb a řešení problémů integrátoru dat](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [Odpovídání na požadavky DSR u systémem generovaných protokolů v PowerApps, Microsoft Flow a Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Správa dat:

  - [Správa dat](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
