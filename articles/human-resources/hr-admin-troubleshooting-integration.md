---
title: Nejčastější dotazy týkající se integrace s aplikací Finance
description: Tento článek vysvětluje, jaká data jsou synchronizována v rámci integrace aplikací Human Resources a Finance.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 946d0433df41ce7067b8b0673db680abb42b7792
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357282"
---
# <a name="integration-with-finance-faq"></a>Nejčastější dotazy týkající se integrace s aplikací Finance

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma uvádí odpovědi na časté otázky spojené s tím, jaká data jsou synchronizována při integraci aplikace Dynamics 365 Human Resources s Dynamics 365 Finance.

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Mohu upravit uživatele aplikace Dynamics 365 Talent v Power Apps?

Č. Pokud upravíte uživatele aplikace Human Resources, integrace mezi Human Resources a Dataverse může selhat. V následující tabulce jsou uvedena výchozí nastavení pro uživatele aplikace Talent.

| Celé jméno | ID přihlášky | ID objektu Azure AD | Identifikátor URI ID přihlášky |
| --- | --- | --- | --- |
| Dynamics 365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Výchozí nastavení pro uživatele aplikace Talent.](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Jsou synchronizovaná všechna data nebo jenom některé datové entity?

Je synchronizována dílčí skupina dat. Seznam všech entit uvádí téma [Integrace s Dynamics 365 Finance](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>Proč se nezobrazují žádná data synchronizovaná s touto funkcí Dataverse?

Ve výchozím nastavení je integrace Dataverse v nových prostředích, která nezahrnují zadaná ukázková data, zakázána. Ve výchozím nastavení je tato možnost zapnutá v nových prostředích zahrnujících ukázková data a synchronizace dat je zahájena při zřizování prostředí. Jakmile bude prostředí připraveno k synchronizaci dat, můžete zapnout integraci. Další informace naleznete v tématu [Konfigurace integrace Dataverse](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Je možné vytvořit nové mapování bez použití šablon

Šablony jsou počátečním bodem. Můžete vytvořit vlastní šablonu, ale při vytváření projektu integrace je šablona potřeba vždy. Další informace o šablonách integrátoru dat (DI) a projektech naleznete v tématu [Integrace dat v Microsoft Dataverse](/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Lze mapovat finanční dimenze k přenosu mezi aplikacemi Human Resources a Finance?

Finanční dimenze aktuálně nejsou v Dataverse pro aplikace a proto nejsou součástí výchozí šablony. Tato entita je plánována, ale v současné době není k dispozici žádná časová osa pro uvolnění.

V případě dat, která existují v modulu Finance, ale ne v aplikaci Human Resources, spojte tyto dva systémy pomocí příkazu **Konfigurovat odkazy** v aplikaci Human Resources.

![Mapovat finanční dimenze.](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Někdy se stane, že když importuji zaměstnance, přejdou v modulu Finance. Proč?

Jestliže zaměstnanci nemají záznam podrobností o aktivním zaměstnání v aplikaci Human Resources může dojít k této chybě. Chybu vyřešíte tak, že přejdete na položky **Správa zaměstnanců \> Zaměstnanci \> Historie zaměstnání \> Správce dat** a ověříte, že existuje aktivní záznam detailů zaměstnání.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Pokud vyberu možnost mapovat pouze dílčí sadu polí, spustí provedené změny provedené v nemapovaných polích synchronizaci?

Synchronizace dat řídí plán provedení. Integrace vyzvedne záznam, pokud se změní některé pole v záznamu, bez ohledu na to, zda je pole součástí mapování integrace.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Jak se dají poslat pouze změny aktivního pracovníka a ne ukončené záznamy?

S použitím "Rozšířeného dotazu" můžete filtrovat a měnit tvar zdrojových dat před předáním do cíle.

![Rozšířený dotaz aktivních pracovníků.](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Můžu určit pole, která chcete odeslat do modulu Finance pro konkrétní entitu?

Pole lze přidat nebo odebrat z úkolu integrace. Ne všechna datová pole, která existují na Dataverse budou doplněna z Human Resources.
Prostřednictvím Power Apps lze naplnit další data.

![Přidání do úkolu integrace a odstranění z něj.](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Mám nastavenou integraci jako dávkovou úlohu, ale aplikace Human Resources ztratila připojení do cílového systému. Jak se dá odeslat stejná sada změny do cílového systému?

Není potřeba žádné speciální nastavení pro zpracování výjimek. Integrátor dat automaticky zachytí a zaznamená chyby, které se objevují ve zdroji a cíli a umožní ruční opakování. Avšak nepovoluje ruční opravy dat. Pokud je nutné provést aktualizace dat, mělo by tak být provedeno ve zdroji nebo v cíli.

## <a name="can-i-set-up-bi-directional-integration"></a>Můžu nastavit integraci obousměrně?

Ne, integrace je nyní jednosměrná (Human Resources do Finance and Operations). Je však k dispozici výchozí šablona pro odeslání dat z aplikace Human Resources do Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Můžu povolit odstranění záznamu v rámci Moje integrace?

Ne, integrátor dat nebude zaznamenávat odstraněné záznamy pro přenos dat. V současné době jsou zahrnuta pouze data vytvoření a aktualizace (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Můžu znovu spustit chybné spuštění? Odešle se v takovém případě celý soubor nebo pouze změny?

Při prvním spuštění aplikace Integrátor dat je vždy úplné spuštění. Dalším spuštění jsou založeny na sledování změn. Při chybě spuštění se záznamy v rozsahu spuštění extrahují a odešlou z Dataverse poslední změny.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Při ukládání projektu se zobrazila chybová zpráva: "Projekt obsahuje chyby mapování". Co udělat?

Zkontrolujte nastavení klíčů integrace, proveďte požadované změny nastavení a aktualizujte entity v projektu.

Při použití výchozí šablony budou integrační klíče automaticky importovány. K tomuto problému může dojít, když jsou do existující šablony přidány nové úkoly.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Pokud mám nekonečný počet právnických osob, kde mají zaměstnanci zaměstnání, je nutné vytvořit mapování pro každý z nich?

Ano, pro každou právnickou osobu v modulu Finance je nutný samostatný integrační projekt v integraci dat.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Je třeba převést data, která nejsou součástí výchozí šablony od společnosti Microsoft. Lze to provést?

Ano, pole můžete přidat do existující šablony nebo z ní odebrat. Šablony lze upravit tak, aby obsahovaly další data z jiných tabulek Dataverse. Entita musí být Dataverse, aby byla zahrnuta do šablony. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Právě jsem vytvořil nová prostředí Finance a Human Resources a zobrazuje se chyba Hodnota data porušuje omezení integrity. Proč?

Důvody této chyby mohou zahrnovat:

- Převod dat měl za následek extrahování duplicitních záznamů ve zdroji (Dataverse).

- Přenos dat má hodnoty null pro pole, která jsou v aplikaci Finance and Operations povinná. Ověřte data, která se jsou v Dataverse a splňují požadavky aplikace Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Pokud došlo k chybám provedení a neproběhla synchronizace ID zaměstnance, jak lze najít úlohu historie s neúspěšným záznamem zaměstnance?

Integrátor dat v modulu Finance vytvoří více projektů. Vztah mezi úlohou integrátoru dat a projektem Finance je jedna ku jedné.

Sledujte čas od historie provedení integrátoru dat a hledejte projekt index - 1 v modulu Finance. Pokud je číslo úlohy v integrátoru dat 9, index modulu operace Finance je 8.

1. Zaznamenejte index úkolů z integrátoru dat (v tomto případě je to "9").

    ![Zaznamenání indexu úkolů z integrátoru dat.](media/CaptureTaskIndex.png)

2. Sledujte čas provádění projektu.

    ![Sledování času provádění projektu.](media/CaptureTimeOfExecution.png)

3. V modulu finance určete index - 1. V tomto příkladu projekt bude mít příponu 8 a čas provedení projektu indexu 0 odpovídá času provedení v kroku 2.

    ![Identifikace indexu.](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>Po integraci aplikací Human Resources a Finance nevidím v aplikaci Finance žádná data z aplikace Human Resources. Co udělat?

Integrace s aplikací Finance je proces ve dvou krocích. Nejprve ověřte, že jsou data aplikace Human Resources aktualizovaná a dostupná v Dataverse. To je synchronizace v reálném čase a lze ji ověřit v Power Apps pohledem na data v rámci datových tabulek.

![Data v Dataverse.](media/DataInCDS.png)

Pokud se data v Dataverse nezobrazují požadovaným způsobem, ověřte, že je entita v integraci podporovaná. Pokud chcete zahrnout do Dataverse další data, bude požadována změna na straně společnosti Microsoft.

Pokud je entita podporovaná a data jsou v Dataverse k dispozici, ověřte, zda je v integrátoru dat správné mapování. Pokud se mapování integrátoru zdá v pořádně, ověřte, zda jsou úspěšně spuštěné úlohy správy dat. Během zpracování dávkových úloh může dojít k chybám. Další informace o způsobu použití nástroje pro správu dat naleznete v tématu [Správa dat](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Údaje o adrese mých zaměstnanců nejdou po importu do aplikace Finance správné. Co mám dělat?

Číselná řada pro **ID skladového místa** používá stejný vzorec v aplikacích Human Resources i Finance. Číselné řady musí být jedinečný na obou stranách tak, aby nebyla žádná kolize adres při integraci dat z Dataverse do Finance and Operations.

Při implementaci aplikace Human Resources ověřte, zda číselné řady v aplikaci Human Resources a Finance nejsou stejné. Ověřte, zda nejsou všechny číselné řady stejné, když lze udržovat data v obou systémech.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Při vytvoření sady připojení nevidím připojení v rozevíracím seznamu připojení. Co udělat?

Při vytváření připojení zvolte Dynamics 365 Finance a Dataverse.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Při synchronizaci zaměstnání se zobrazují chyby "CompanyInfo_FK neexistuje" nebo "Hodnota 31/12 a 2154 23:59:59: 00 ' v poli Koncové datum zaměstnání nebyla nalezena v související tabulce"Zaměstnání"." Co mám dělat?

Mapujte na správné právnické osoby. Synchronizace právnické osoby není součástí výchozí šablony, takže se očekává, že každá právnická osoba přítomná v aplikacích Human Resources a Dataverse je dostupná také v aplikaci Finance.
Dále také vyberte správné právnické osoby pro přidruženou sadu připojení.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Po nastavení projektu se zdá mapování polí pro Finance prázdné. Co mám dělat?

Aktualizujte entity dat v aplikaci Finance v části **Správa dat \> Parametry systému \> Nastavení entity \> Aktualizovat seznam entit.** Mělo by to trvat několik minut a poté by se mělo zobrazit toto mapování. K tomuto problému dochází při vytváření nových projektů.

![Mapování chybějících polí.](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Další prostředky

- Integrátor dat (Di): 

  - [Integrace dat do Microsoft Dataverse](/powerapps/administrator/data-integrator)

  - [Správa chyb a řešení problémů integrátoru dat](/powerapps/administrator/data-integrator-error-management)

  - [Odpovídání na požadavky DSR u systémem generovaných protokolů v Power Apps, Microsoft Power Automate a Dataverse](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Správa dat:

  - [Správa dat](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]