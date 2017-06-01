---
title: "Zastaralé funkce"
description: "Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění v Dynamics 365 for Operations. Obsahuje také seznam funkcí, které byly odstraněny ze starších verzí Dynamics AX 7.0."
author: sericks007
manager: AnnBe
ms.date: 04/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Platform
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 46a6f054f1cc5162e19d962964eb6eeb780087a6
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="deprecated-features"></a>Zastaralé funkce

[!include[banner](../includes/banner.md)]


Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění v Dynamics 365 for Operations. Obsahuje také seznam funkcí, které byly odstraněny ze starších verzí Dynamics AX 7.0.

<a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Funkce, které jste již nepoužívají v Dynamics 365 for Operations 1611 po aktualizaci platformy 3
---------------------------------------------------------------------------------------------

### <a name="aeb-payment-formats-for-spain"></a>AEB formáty plateb pro Španělsko

Pro odesílání souborů úhrad s platbami odběratelů a dodavatelů do banky se používají formáty CSB (Consejo Superior Bancario). Obsah těchto formátů je stanoven asociací AEB (Asociación Española de Banca). Zahrnuty jsou také Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                                  |
| Nahrazeno jinou funkcí? | Ano, ISO20022 formáty bezhotovostních převodů a přímých debetních plateb pro Španělsko |
| Ovlivněné moduly             | Pohledávky, závazky                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankovní převod plateb pro Litvu

Bankovní platební převody generované a tisknuté za použití formátu exportu platebního převodu pro Litvu (LT). Litevský trh začal v roce 2005 používat LITAS, sjednocený elektronický bankovní systém.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                    |
| Nahrazeno jinou funkcí? | Ano, Litevský formát platby peněžního převodu ISO20022. |
| Ovlivněné moduly             | Závazky                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Formáty plateb BBS Direkte Remittering pro Norsko

Formáty plateb BBS Direkte Remittering zahrnují export inkasní platby odběratele (inkaso) a import zprávy o vrácení.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                                                                                                                        |
| Nahrazeno jinou funkcí? | Formát platby odběratele AvtaleGiro pro Norsko lze využít ke generování zprávy o souhlasu s inkasem. Import zprávy o vrácení bude zahrnut do příštích verzí. |
| Ovlivněné moduly             | Pohledávky, závazky                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Nástroj účtové osnovy pro Španělsko

Tento nástroj se používá, když účtová osnova ve Španělsku vyžaduje zásadní změny. Uživatelé mohou importovat nové účtové osnovy v aplikaci Microsoft Excel nebo v textovém formátu a mohou také importovat finanční výkazy.

|                              |                |
|------------------------------|----------------|
| Důvod pro zrušení       | Omezené použití  |
| Nahrazeno jinou funkcí? | Žádný             |
| Ovlivněné moduly             | Hlavní kniha |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 formát platby pro Belgii

Starý belgický formát platby pro inkaso platby (přímý debet).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Důvod pro zrušení       | Formát plateb se již nepoužívá.                  |
| Nahrazeno jinou funkcí? | Ano, specificky belgický formát inkasní platby ISO 20022. |
| Ovlivněné moduly             | Pohledávky                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG formáty plateb pro Švýcarsko

Formáty odložených daňových aktiv/EZAG jsou integrovány do systému ESR, jelikož mohou obsahovat referenční číslo. Jelikož referenční číslo není povinné, mohou být pomocí těchto formátů zpracovány všechny platby dodavatele. Tyto formáty využívají společnosti, které máte bankovní účet ve skladovém místě jiném než "Postfinance".

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                      |
| Nahrazeno jinou funkcí? | Ano, švýcarský formát platby peněžního převodu ISO20022 |
| Ovlivněné moduly             | Závazky                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Specificky rakouský formát inkasní platby EDIFACT-DIRDEB.

EDIFACT-DIRDEB formát platby pro inkaso platby (přímý debet).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Důvod pro zrušení       | Formát plateb se již nepoužívá.                  |
| Nahrazeno jinou funkcí? | Ano, specificky rakouský formát inkasní platby ISO 20022. |
| Ovlivněné moduly             | Pohledávky                                    |

### <a name="edivat-for-belgium"></a>EDIVAT pro Belgii

EDIVAT je starý standard pro elektronické prohlášení prostřednictvím zabezpečení pošty v Belgii. Microsoft Dynamics AX 2012 zachovává řešení jen pro čtení pro umožnění přístupu k historickým datům.

|                              |                                      |
|------------------------------|--------------------------------------|
| Důvod pro zrušení       | Tato funkce se již nepoužívá. |
| Nahrazeno jinou funkcí? | Žádný                                   |
| Ovlivněné moduly             | Hlavní kniha                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Importní formát platby eGiro EDIFACT CREMUL pro Norsko

eGiro je založeno na mezinárodních standardech SN EDIFACT CREMUL (Multiple Credit Advice Message), které slouží pro automatické zaúčtování plateb odběratele. V aplikaci Microsoft Dynamics AX je eGiro implementováno jako formát importu platby odběratele.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formát plateb se již nepoužívá.                                                     |
| Nahrazeno jinou funkcí? | Č. Formát bude nahrazen formátem importu výpisu ISO 20022 v příštích verzích. |
| Ovlivněné moduly             | Pohledávky                                                                       |

### <a name="external-inventory-for-poland"></a>Externí zásoby v Polsku

Doklad o zboží, který je přijatý od dodavatele pro účely prodeje bez nákupu. Zboží, které je zpracováno v externím skladu, nemá vliv na standardní zásoby a lze ho prodat a pak zakoupit automaticky. Tento proces vytváří skutečné pohyby zásob.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| Důvod pro zrušení       | Nahrazeno jinou funkcí                     |
| Nahrazeno jinou funkcí? | Ano, základní funkce příchozí zásilky |
| Ovlivněné moduly             | Závazky, řízení zásob          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Generátor finančních sestav pro východní Evropu

Nástroj se používá pro nastavení shromažďování dat pro účetnictví a daňové sestavy a export dat do šablon sestavy XLS a DOC

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Omezené použití                                                                            |
| Nahrazeno jinou funkcí? | Č. Tento nástroj bude nahrazen konfigurací elektronických sestav v budoucích verzích. |
| Ovlivněné moduly             | Hlavní kniha                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import transakce plateb odběratelů pro Finsko

Můžete vybrat formát importu pro platby ve Finsku, ve kterém se importují platební transakce odběratelů z externího souboru, který zajišťuje banka.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formát plateb se již nepoužívá.                                                     |
| Nahrazeno jinou funkcí? | Č. Formát bude nahrazen formátem importu výpisu ISO 20022 v příštích verzích. |
| Ovlivněné moduly             | Pohledávky                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import platebních transakcí do deníku hlavní knihy pro Finsko

Formát, který je specifický pro Finsko, se používá k importu transakcí účtování do hlavní knihy.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formát plateb se již nepoužívá.                                                     |
| Nahrazeno jinou funkcí? | Č. Formát bude nahrazen formátem importu výpisu ISO 20022 v příštích verzích. |
| Ovlivněné moduly             | Pohledávky                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integrace s Isabel synchronizována (CIS) pro Belgii

Isabel je platforma pro elektronické bankovnictví v Evropě a je de facto standardní v Belgii.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Integrace s klientem Isabel již není nabízena.                                                                |
| Nahrazeno jinou funkcí? | Ne. Formáty plateb, které se již nepoužívají, jsou nahrazeny ISO20022 formátem platebního převod platby pro Belgii. |
| Ovlivněné moduly             | Závazky                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Změny v účetní osnově a účetních pravidlech pro Španělsko

Tato funkce se používá pro změny v účtové osnově a účetních pravidlech ve Španělsku. Mapuje účty, aby pomohla transformovat původní účtovou osnovu do nové účtové osnovy a porovnává předchozí fiskální rok s novým fiskálním rokem i v případě, že byly zaúčtovány na různá čísla účtů.

|                              |                |
|------------------------------|----------------|
| Důvod pro zrušení       | Omezené použití  |
| Nahrazeno jinou funkcí? | Žádný             |
| Ovlivněné moduly             | Hlavní kniha |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Formát platby dodavatele Pagamento Fornittori

Starý italský formát platby peněžních převodů.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Důvod pro zrušení       | Formát plateb se již nepoužívá.                  |
| Nahrazeno jinou funkcí? | Ano, italský formát platby peněžního převodu ISO20022. |
| Ovlivněné moduly             | Závazky                                       |

### <a name="payment-export-formats-for-estonia"></a>Formáty pro export plateb v Estonsku

Formáty Telehansa a Teleservice se používají pro export bankovních plateb.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                  |
| Nahrazeno jinou funkcí? | Ano, specificky estonský formát platby peněžního převodu ISO20022. |
| Ovlivněné moduly             | Závazky                                         |

### <a name="payment-file-archive-for-norway"></a>Archiv souborů plateb pro Norsko

Když dojde ke generování souborů plateb, archiv souborů automaticky archivuje všechny soubory, které jsou vytvořeny, i soubory, které byly dříve zapsány nebo načteny.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| Důvod pro zrušení       | Nahrazeno jinou funkcí                                        |
| Nahrazeno jinou funkcí? | Ano, archivované úlohy elektronického výkaznictví                            |
| Ovlivněné moduly             | Závazky, pohledávky, správa organizace |

### <a name="payment-import-formats-for-estonia"></a>Formáty pro import plateb v Estonsku

Formáty Telehansa a TeleTeenus se používají pro import bankovních plateb.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                                                    |
| Nahrazeno jinou funkcí? | Č. Formáty budou nahrazeny formátem importu výpisu ISO 20022 v příštích verzích. |
| Ovlivněné moduly             | Pohledávky                                                                        |

### <a name="performance-management-goal-workflow"></a>Pracovní postup cíle řízení výkonnosti

Řízení výkonnosti zahrnuje správu cílů a integraci s hodnocením výkonu.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Řízení výkonnosti bylo změněno a počet stránek cílů se snížil, aby došlo ke zjednodušení procesu.                 |
| Nahrazeno jinou funkcí? | Ne. Cíle jsou viditelné pro vedoucí pracovníky pomocí portálu samoobslužných stránek správce a lze je změnit a zobrazit manažerem. |
| Ovlivněné moduly             | Správa lidského kapitálu                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Formáty platby Postgirot a Postgirot Utland pro Švédsko

Formáty platby Postgirot a Postgirot Utland pro Švédsko.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                 |
| Nahrazeno jinou funkcí? | Ano, specificky švédský formát platby peněžního převodu ISO20022. |
| Ovlivněné moduly             | Závazky                                        |

### <a name="radio-frequency-identifier"></a>Radiofrekvenční identifikátor

Radiofrekvenční identifikace (RFID) představuje technologii shromažďování dat, která využívá elektronických značek k uložení identifikačních dat a nevyžaduje žádné zařízení ke čtení identifikačních dat, které by muselo být v přímé viditelnosti k označenému předmětu.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| Důvod pro zrušení       | Málo používáno odběrateli a omezená sada funkcí. |
| Nahrazeno jinou funkcí? | Žádný                                            |
| Ovlivněné moduly             | Řízení zásob                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Zpráva o číslování státních faktur Lotyšska

Lotyšská legislativa poskytuje konkrétní pravidla týkající se číslování prodejních faktur. Funkce umožňuje přiřadit specifická čísla do prodejních faktur na základě uživatele nebo skupiny uživatelů. Pak lze vygenerovat sestavu nebo soubor XML. Lze také vytisknout sestavy s informacemi o použitých číslech faktur.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Není už nutné zachovávat číslování státních faktur. Hlášení o použitých číslech faktur již není požadováno. |
| Nahrazeno jinou funkcí? | Žádný                                                                                                                       |
| Ovlivněné moduly             | Pohledávky                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Nastavení jmen správce a hlavního účetního společnosti pro Litvu

Jména správce a hlavního účetního společnosti mohou být určena v informacích o společnosti a využita ve výtiscích různých místních sestav.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Důvod pro zrušení       | Nahrazeno jinou funkcí                                     |
| Nahrazeno jinou funkcí? | Ano, nastavení úředních osob lze použít k tomuto účelu.   |
| Ovlivněné moduly             | Závazky, Pohledávky, Řízení zásob, Pokladna a banka |

### <a name="telepay-payment-formats-for-norway"></a>Telepay formáty plateb pro Norsko

Telepay formáty plateb zahrnují exporty plateb dodavatele (převod) a inkasa plateb odběratele (přímý debet).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                                                        |
| Nahrazeno jinou funkcí? | Ano, formátu platby platebního převodu ISO20022 a formát platby odběratele AvtaleGiro pro Norsko |
| Ovlivněné moduly             | Pohledávky, závazky                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Formáty exportu plateb dodavatele pro Finsko

Existují dva formáty pro export plateb pro Finsko. LM02 (FI) se používá pro domácí platby a LUM2 (FI) se používá pro zahraniční platby.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Důvod pro zrušení       | Formáty plateb se již nepoužívají.                  |
| Nahrazeno jinou funkcí? | Ano, finský formát platby peněžního převodu ISO20022 |
| Ovlivněné moduly             | Závazky                                         |

### <a name="workflow-for-creating-goals"></a>Postup pro vytváření cíle

Workflow správy vytvoření cílů zaměstnanců je jednou z několika workflowů, které byly k dispozici pro pomoc koordinovat proces řízení výkonnosti.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Řízení výkonnosti bylo zcela změněno v aplikaci Microsoft Dynamics 365 for Operations.                                                                                                                                                                                                                                        |
| Nahrazeno jinou funkcí? | Upravená funkce řízení výkonnosti poskytuje větší kontrolu nad obsahem cílů, měřeními, která se používají ke sledování vývoje, a připojováním podpůrné dokumentace. Cíle lze ukládat jako šablony a pak znovu použít. Tato funkce vám pomůže rychleji nastavit další cíle pro zaměstnance. |
| Ovlivněné moduly             | Správa lidského kapitálu                                                                                                                                                                                                                                                                                                               |

## <a name="features-deprecated-in-dynamics-ax-70-releases"></a>Funkce, které se již nepoužívají v aplikaci Dynamics AX ve verzi 7.0
### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Možnost zrušení změn na faktuře dodavatele

|                              |                         |
|------------------------------|-------------------------|
| Důvod pro zrušení       | Zvýšení výkonnosti |
| Nahrazeno jinou funkcí? | Č.                      |
| Ovlivněné moduly             | Závazky        |

### <a name="aif-axd-and-axbc-integrations"></a>Integrace rozhraní AIF, AxD a AxBC

V rozhraní AIF (Application Integration Framework) mohou být data vyměňována s externími systémy pomocí obchodní logiky, která je zveřejněna jako služba. Dynamics AX obsahuje služby, které jsou založeny na dokumentech a programu .NET Business Connector (AxBC). Dokument je vytvářen pomocí kódu XML. Soubor XML obsahuje informace v záhlaví, které jsou přidány pro vytvoření *zprávy*, již lze přenést do a z aplikace Dynamics AX. Příkladem takovýchto dokumentů mohou být prodejní objednávky nebo nákupní objednávky. Dokumentem však může být reprezentována téměř jakákoliv entita, například odběratel. Služby, které jsou založeny na dokumentech, používají třídy **Axd &lt;*Dokument*&gt;**.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Architekturu rozhraní AIF a AxDs nelze škálovat do cloudové služby. Při hromadném importu docházelo k problémům s výkonem.                                                                               |
| Nahrazeno jinou funkcí? | V aktuální verzi aplikace Dynamics AX je tuto funkce nahrazena architekturou pro import a export dat, která podporuje opakovaný hromadný import/export. U rozhraní AxBC doporučujeme používat skutečné tabulky. |
| Ovlivněné moduly             | AxDs, AxBCs a AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Kusovníky bez verze kusovníku

Pokud byl konfigurační klíč **Verze kusovníku** zakázán, byly ve všech formulářích skryty verze kusovníku a systém vynutil vztahy 1:1 mezi uvolněnými produkty a kusovníky. V aktuální verzi aplikace Dynamics AX nelze konfigurační klíč **Verze kusovníku** zakázat.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Řízení verzí kusovníku pomocí konfiguračního klíče nelze škálovat v cloudovém prostředí. |
| Nahrazeno jinou funkcí? | Č.                                                                                      |
| Ovlivněné moduly             | Řízení informací o produktech, Řízení zásob                                    |

### <a name="brazilian-bordero"></a>Brazilský doklad Bordero

Specifická metoda platby pro brazilské společnosti

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Podpora pro brazilskou metodu platby Bordero již není k dispozici v brazilské lokalizaci |
| Nahrazeno jinou funkcí? | Žádný                                                                                                    |
| Ovlivněné moduly             | Závazky                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brazilský výpis Sintegra

Federální daňový výkaz ICMS

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Toto prohlášení se již v některých brazilských zemích nepoužívá.                                                     |
| Nahrazeno jinou funkcí? | Ne. Uživatelé mohou používat nástroj obecného elektronického vykazování pro konfiguraci výkazu, pokud je v určitých situacích požadován. |
| Ovlivněné moduly             | Fiskální knihy                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brazilský pohotovostní režim SCAN pro NF e

Pohotovostní prostředí (SCAN) slouží k vygenerování, exportování a importování stavu Nota Fiscal eletrônica (NF-e), pokud není k dispozici prostředí Secretaría da Fazenda (SEFAZ).

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| Důvod pro zrušení       | Tato záložní metoda už nebude k dispozici v žádném brazilském státě |
| Nahrazeno jinou funkcí? | Žádný                                                                          |
| Ovlivněné moduly             | Pohledávky                                                         |

### <a name="business-analyzer"></a>Obchodní analýza

S touto mobilní aplikací mohou uživatelé kontrolovat klíčoví obchodní metriky.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Tato funkce byla nahrazena jinou funkcí.                                                                                                      |
| Nahrazeno jinou funkcí? | Balíček obsahu Sledování finanční výkonnosti pro Microsoft Power BI bude zahrnovat klíčové finanční metriky, které byly dříve dostupné v aplikaci Business Analyzer. |
| Ovlivněné moduly             | Hlavní kniha                                                                                                                                                |

### <a name="business-statistics"></a>Obchodní statistika

Nastavení dotazů na obchodní statistiky, která vám mohou pomoct s analýzou výkonnosti organizace

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Starší přístup k obchodnímu zpravodajství (BI), málo používáno odběrateli a omezená sada funkcí |
| Nahrazeno jinou funkcí? | Nové řešení BI pro aktuální verzi aplikace Dynamics AX                                      |
| Ovlivněné moduly             | Zásobování a zdroje, Závazky, Prodej a marketing, Pohledávky         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Funkce změny data dokumentu v modulu Deník schválených faktur

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Důvod pro zrušení       | Malé využití                                                               |
| Nahrazeno jinou funkcí? | Ano. Datum dokumentu na zaúčtované transakci dodavatele lze změnit. |
| Ovlivněné moduly             | Závazky                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Formát platby ClieOp03 pro Nizozemsko

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formát se již v Nizozemsku nepoužívá, protože byl nahrazen funkcí Jednotná oblast pro platby v eurech (SEPA). |
| Nahrazeno jinou funkcí? | Export plateb SEPA                                                                                       |
| Ovlivněné moduly             | Vše                                                                                                        |

### <a name="compliance-center"></a>Centrum kompatibility

Centrum kompatibility byly stránky podnikového portálu pro správu požadavků na dokumentaci pro iniciativy kompatibility související se Sarbanes-Oxleyho zákonem.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Nepoužíváno odběrateli. Služba Microsoft SharePoint zahrnuje stejné možnosti, jaké byly k dispozici v centru kompatibility. |
| Nahrazeno jinou funkcí? | Č.                                                                                                                     |
| Ovlivněné moduly             | Dodržování předpisů a vnitřní kontroly                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Connector pro aplikaci Microsoft Dynamics

Tento nástroj byl použit k integraci klíčových dat z aplikace Microsoft Dynamics CRM do aplikace Microsoft Dynamics ERP.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Důvod pro zrušení       | Tato funkce byla nahrazena jinou funkcí. |
| Nahrazeno jinou funkcí? | Integrátor Dynamics                                      |
| Ovlivněné moduly             | Connector pro aplikaci Microsoft Dynamics                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Jednotka kontejneru a více dimenzí zásob

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Duplicitní funkce                                                                                                                                         |
| Nahrazeno jinou funkcí? | Ano. Tuto funkce byla nahrazena od verze AX 2012 sadou funkcí konsolidované dávkové objednávky. Tato sada funkcí zahrnuje konsolidované zobrazení zásob na skladě. |
| Ovlivněné moduly             | Řízení informací o produktech, Řízení výroby, Řízení zásob, Prodej a marketing                                                                   |

### <a name="cue-group-metadata"></a>Metadata skupiny hromádek

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Skupiny hromádek byly použity k zobrazení jedné nebo více hromádek v oblasti okna s fakty. Byl omezený příjem a došlo k také k potížím s výkonem kvůli změně záznamu v nadřazeném formuláři, což způsobilo jeden dotaz na každou hromádku ve skupině hromádek. |
| Nahrazeno jinou funkcí? | Č.                                                                                                                                                                                                                            |
| Ovlivněné moduly             | Vše                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Metadata hromádky

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Metadata hromádky byla omezena na informace o počtu nebo součtu.                                                                                                                                                                                   |
| Nahrazeno jinou funkcí? | Kvůli flexibilnějším možnostem modelování byla zavedena metadata dlaždice. Modelova můžete například aktuální počty, navigaci a klíčové indikátory výkonnosti (KPI). Metadata dlaždice počtu jsou přímou náhradou za metadata hromádky. |
| Ovlivněné moduly             | Vše                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Formát šeku – Dánsko

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Byla zrušena podpora pro rozvržení dánského formátu šeku a sestava byla odebrána z dánské lokalizace. |
| Nahrazeno jinou funkcí? | Č.                                                                                                                      |
| Ovlivněné moduly             | Vše                                                                                                                     |

### <a name="data-partitions"></a>Datové oddíly

Datové oddíly poskytují logické oddělení dat v databázi aplikace Microsoft Dynamics AX.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Datové oddíly byly zavedeny v aplikaci Microsoft Dynamics AX 2012 R2 a umožňují izolaci dat. V běžné situaci má společnost pobočky a data z jedné dceřiné společnosti by neměla být viditelná pro jiné dceřiné společnosti, přestože obě pobočky jsou spravovány ve stejném oddělení IT. Nicméně by byly vyžadovány dodatečné skripty a další správní režie v celém programu pro vytvoření nových oddílů, naplnění je daty a zálohování data oddílu. V cloudu, kde máte přístup k databázové službě Platforma jako služba (PaaS – Microsoft Azure SQL Database), je mnohem efektivnější použít databázi pro izolační kontejner, než provádět izolaci v programu. Bez ohledu na to, zda je rozdělení dat požadované pro dceřiné společnosti, pro více klientů nebo pouze pro škálování, věříme, že situace je možné vyřešit efektivněji s využitím více databází nebo instancí aplikace Dynamics AX. |
| Nahrazeno jinou funkcí? | Datové oddíly budou v budoucí verzi nahrazeny prostřednictvím podpory více databází nebo instancí aplikace Dynamics AX.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ovlivněné moduly             | Vše                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

### <a name="delimitation"></a>Vymezení

|                              |                                        |
|------------------------------|----------------------------------------|
| Důvod pro zrušení       | Funkce nebyla shledána potřebnou. |
| Nahrazeno jinou funkcí? | Č.                                     |
| Ovlivněné moduly             | Čas a docházka                    |

### <a name="desktop-client"></a>Klient pro stolní počítače

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Prostředí klienta aplikace Dynamics AX bylo přepracováno, aby se lépe používalo na různých platformách a v různých zařízeních.                      |
| Nahrazeno jinou funkcí? | Nový webový klient je založen na metadatech formuláře pracovní plochy a programovacím modelu, které byly změněny tak, aby poskytovaly bohatou webovou platformu. |
| Ovlivněné moduly             | Vše                                                                                                                                    |

### <a name="direct-database-connection"></a>Přímé připojení k databázi

V aplikaci Dynamics AX 2012 R3 se Retail Modern POS připojoval přímo k databázi Channel DB podobným způsobem jako k Enterprise POS. Byla to nástavba ke standardní metodě komunikace Retail Modern POS prostřednictvím Retail Serveru.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Přímé připojení k databázi vyžadovalo nižší protokoly zabezpečení a primárně sloužilo k dosahování nejvyšších úrovní výkonnosti. Vzhledem k výkonu a vylepšení zabezpečení, ke kterým došlo v aplikaci Dynamics 365 for Operations tato funkce nyní způsobuje mnohem více problémů, než řeší. |
| Nahrazeno jinou funkcí? | Č. V současné době se podporuje pouze standardní komunikace Retail Server.    |
| Ovlivněné moduly             | Channel DB/Retail Modern POS                                    |

### <a name="dutch-swift-mt940"></a>Nizozemský SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Namísto lokalizované funkce se nyní používá obecná funkce.                                                                                                                                                                 |
| Nahrazeno jinou funkcí? | Ano, tato funkce byla nahrazena funkcí Rozšířené odsouhlasení banky. Kromě toho je v další aktualizaci aplikace Dynamics AX naplánována implementace importu výpisů z účtu camt.053 ISO20022 pro Hlavní deník. |
| Ovlivněné moduly             | Vše                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL pro Německo)

Tato funkce poskytuje výstup v jazyce eXtensible Business Reporting Language (XBRL), který je určený konkrétně pro německou taxonomii eBilanz.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Nepoužíváno odběrateli.                                                                                                                                                 |
| Nahrazeno jinou funkcí? | Tato funkce nebyla nahrazena jinou funkcí, avšak pro německý trh je k dispozici několik speciálních balíčků XBRL obsahujících mnoho funkcí XBRL. |
| Ovlivněné moduly             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Klient podnikového portálu

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Byla poskytnuta jediná platforma klienta.                                                                                            |
| Nahrazeno jinou funkcí? | Nový webový klient je založen na metadatech formuláře pracovní plochy a programovacím modelu, které byly změněny tak, aby poskytovaly bohatou webovou platformu. |
| Ovlivněné moduly             | Vše                                                                                                                                    |

### <a name="environmental-sustainability"></a>Udržitelnost životního prostředí

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| Důvod pro zrušení       | Málo používáno odběrateli a omezená sada funkcí.       |
| Nahrazeno jinou funkcí? | Č.                                                 |
| Ovlivněné moduly             | Dodržování předpisů a vnitřní kontroly, Závazky |

### <a name="form-activex-and-managed-host-controls"></a>Ovládací prvky formuláře ActiveX a spravovaného hostitele

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Ovládací prvky formuláře ActiveX a spravovaného hostitele jsou založeny na zastaralém klientovi pro stolní počítače.                                                                                                             |
| Nahrazeno jinou funkcí? | Rozšířitelná architektura ovládacích prvků podporuje vytváření nových ovládacích prvků založených na jazyku HTML, CSS a JavaScript a slouží k prvotřídnímu ovládání v prostředí nástroje Microsoft Visual Studio. |
| Ovlivněné moduly             | Vše                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Generování verifikačních transakcí pomocí dávky

Verifikační transakce nelze generovat pomocí dávky, ale mohou být generovány uživatelem.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Neexistuje žádný formulář, který by po vygenerování pomocí dávky zachovával a zobrazoval výsledný soubor verifikačních transakcí. |
| Nahrazeno jinou funkcí? | Verifikační transakce lze i nadále generovat a uživatel může nastavit umístění, kam má být soubor uložen.   |
| Ovlivněné moduly             | Závazky, Pohledávky, Řízení zásob, Pokladna a banka                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Export německé platby DTAUS a import výpisu z účtu (souhrny a transakce)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formát se již v Německu nepoužívá, protože byl nahrazen funkcí Jednotná oblast pro platby v eurech (SEPA).                                                                                                                                                                 |
| Nahrazeno jinou funkcí? | Ano, tato funkce byla nahrazena exportem plateb SEPA a rozšířenou funkcí odsouhlasení banky pro import výpisů z účtu. Kromě toho je v další aktualizaci aplikace Dynamics AX naplánována implementace importu výpisů z účtu camt.053 ISO20022 pro Hlavní deník. |
| Ovlivněné moduly             | Vše                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Německý formát platby DTAZV

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formát se již v Německu nepoužívá, protože byl nahrazen funkcí Jednotná oblast pro platby v eurech (SEPA). |
| Nahrazeno jinou funkcí? | Export plateb SEPA                                                                               |
| Ovlivněné moduly             | Vše                                                                                                |

### <a name="german-mt940-import"></a>Německý import MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Namísto lokalizované funkce se nyní používá obecná funkce.                                                                                                                                                                 |
| Nahrazeno jinou funkcí? | Ano, tato funkce byla nahrazena funkcí Rozšířené odsouhlasení banky. Kromě toho je v další aktualizaci aplikace Dynamics AX naplánována implementace importu výpisů z účtu camt.053 ISO20022 pro Hlavní deník. |
| Ovlivněné moduly             | Vše                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Německé souhrnné hlášení (EU) ve formátu XML

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Formát XML pro německé souhrnné hlášení již není podporován. K odeslání německého souhrnného hlášení německému daňovému úřadu lze použít pouze formát textového souboru ELMA5. |
| Nahrazeno jinou funkcí? | Č.                                                                                                                                                                                 |
| Ovlivněné moduly             | Daň                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>Sestavy GL SSRS

Byly odebrány sestavy, které zahrnují následující položky nabídky: **Souhrnná předvaha**, **Podrobná předvaha**, **Účtové osnovy**, **Záznam pro audit**, **Zůstatky** a **Výpis zůstatků**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Finanční sestavy Microsoft SQL Server Reporting Services (SSRS) byly nahrazeny funkcemi nástroje Management Reporter a výchozími sestavami. |
| Nahrazeno jinou funkcí? | Management Reporter (v aktuální verzi aplikace Dynamics AX označena jako **Finanční výkaznictví**)                                                  |
| Ovlivněné moduly             | Hlavní kniha                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>Metadata InfoPart a FormPart

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Metadata InfoPart a FormPart povolovala vytváření okna s fakty pro dva různé klienty.                                                                                                                                    |
| Nahrazeno jinou funkcí? | Metadata InfoPart, která byla zjednodušenou definicí formuláře, je převedena do formuláře při upgradu nástrojů. Metadata FormPart, která odkazovala na formulář, jsou nahrazena přímějším odkazem, který je vytvářen při upgradu nástrojů. |
| Ovlivněné moduly             | Vše                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Stránka seznamu hlavních účtů

Seznam účtů pro právnickou osobu a související informace o zůstatku

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Informace o zůstatku jsou k dispozici na stránce seznamu **Předvaha** podle účtu a dimenze.                                                                                      |
| Nahrazeno jinou funkcí? | **Hlavní účty** obsahuje seznamu účtů, **hlavní účet** obsahuje stránku se seznamem. V zobrazení v podobě mřížky se na stránce **Hlavní účty** zobrazuje rovněž i menší pohled podobný mřížce. |
| Ovlivněné moduly             | Hlavní kniha                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Sestava bankovního cashflowu v Malajsii a Singapuru

S touto funkcí mohou uživatelé tisknout sestavu cashflowu, v níž jsou uvedeny transakce a podrobnosti o přírůstcích a úbytcích hotovosti pro určený časový interval pro vybraný bankovní účet.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Důvod pro zrušení       | Stejné informace lze získat z funkce Dotaz na bankovní transakce. |
| Nahrazeno jinou funkcí? | Dotaz na bankovní transakce                                            |
| Ovlivněné moduly             | Pokladna a banka                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Mexická elektronická faktura CFD

Tato funkce povolovala generování mexické elektronické faktury pomocí metody CFD (Comprobante Fiscal Digital), u které společnost podepisuje faktury žádostí o příslušné schválení od vlády. Tato funkce rovněž poskytuje měsíční sestavu, která obsahuje všechny elektronické faktury, které byly v daném období vydány.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Metoda již není použitelná. Generování elektronických faktur metodou CFD bylo zrušeno ze strany finančního úřadu a nahrazeno metodou Comprobante Fiscal Digital a través de Internet (CFDI), u které je podepisování delegováno na poskytovatele třetí strany (PAC). Měsíční sestava byla odebrána, uživatelé mohou prostřednictvím dotazu získat informace o historických transakcích. |
| Nahrazeno jinou funkcí? | Č.                                                                                                                                                                                                                                                                                                                                                                                                        |
| Ovlivněné moduly             | Pohledávky, Projekt                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Uplatněná a neuplatněná DPH v Mexiku

Aplikace Microsoft Dynamics AX 2012 spravovala neuplatněnou daň z přidané hodnoty (DPH) pomocí funkce pro neuplatněnou daň specifické pro Mexiko.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Duplicitní funkce                                                                                             |
| Nahrazeno jinou funkcí? | Ano, tato funkce byla nahrazena standardní funkcí podmíněné DPH, která je k dispozici ve verzi Core. |
| Ovlivněné moduly             | Daň                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Integrace aplikace Microsoft Outlook

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| Důvod pro zrušení       | Tato funkce byla nahrazena integrací serveru Microsoft Exchange. |
| Nahrazeno jinou funkcí? | Ano                                                                            |
| Ovlivněné moduly             | Prodej a marketing                                                            |

### <a name="payroll-information-in-human-resources"></a>Mzdové informace v modulu Lidské zdroje

Mzdové informace lidských zdrojů

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Tato funkce byla nahrazena základními stránkami Mzdy a Lidské zdroje.                                                                                                                                                                                                                                              |
| Nahrazeno jinou funkcí? | **Výhody**, **Příjmy** a další související stránky, které byly dříve v modulu Mzdy v USA, byly překonfigurovány a jsou nyní součásti základní konfigurace modulu Lidské zdroje pro podporu zpracování externích mezd. K této funkci se dostanete pomocí konfiguračního klíče **Lidské zdroje 1** &gt; **Mzdy**. |
| Ovlivněné moduly             | Lidské zdroje, Mzdy                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Soukromé blokování deníků řízení zásob a skladu

Deníky skladů a zásob již nepodporují možnost označení deníku jako soukromého pro vybraného uživatele. Je podporován pouze proces blokování deníků jako soukromých pro skupiny uživatelů a blokování během úprav.

|                              |                                        |
|------------------------------|----------------------------------------|
| Důvod pro zrušení       | Funkce nebyla shledána potřebnou. |
| Nahrazeno jinou funkcí? | Č.                                     |
| Ovlivněné moduly             | Řízení zásob                   |

### <a name="product-builder"></a>Konfigurátor výrobku

Konfigurátor výrobku byl používán k dynamické konfiguraci položek z prodejní objednávky, nákupní objednávky, výrobní zakázky, prodejní nabídky, nabídky projektu nebo požadavku na položku. Na základě modelu produktu s proměnnými modelování mohl uživatel volit hodnoty podle potřeb odběratele a získat jedinečnou variantu produktu s vlastním kusovníkem a postupem.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Konfigurátor výrobku zveřejňoval kód X ++ koncovým uživatelům a není v aktuální verzi aplikace Dynamics AX podporován. Byl odebrán kvůli zamezení duplicitní údržby na překrývajících se kódech. |
| Nahrazeno jinou funkcí? | Konfigurace produktu                                                                                                                                                                                   |
| Ovlivněné moduly             | Řízení informací o produktech, Prodej a marketing                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Změnit název dimenze produktu

Touto funkcí lze měnit název jedné ze tří standardních dimenzí produktu (velikosti, barva nebo styl) tak, aby lépe vyhovoval obchodním požadavkům. Přejmenování zahrnovalo všechny popisky, kde by použit název dimenze produktu.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Důvod pro zrušení       | Aktuální verze aplikace Dynamics AX nepodporuje změny popisků v době běhu. |
| Nahrazeno jinou funkcí? | Žádný                                                                            |
| Ovlivněné moduly             | Řízení informací o produktech                                                |

### <a name="retail-server-connectivity-using-http"></a>Konektivita Retail Server u využívající HTTP

V aplikaci Dynamics AX 2012 R3 může Retail Server fungovat pomocí komunikace HTTP (nezabezpečené). Byl to dodatek ke standardní komunikaci pomocí připojení HTTPS.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Důvod pro zrušení       | Z důvodu nových požadavků na zabezpečení je nyní podporována pouze zabezpečená komunikace pomocí TLS 1.2 (nebo vyšší podle dostupnosti). Samoobslužný instalační program bude automaticky konfigurovat počítač na tuto komunikaci. |
| Nahrazeno jinou funkcí? | Č. V současné době se podporuje pouze standardní komunikace HTTPS.                                                                           |
| Ovlivněné moduly             | Server maloobchodu                                                |

### <a name="role-center-pages"></a>Stránky pracovní plochy role

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Stránky pracovní plochy rolí byly vytvořeny na zastaralé platformě podnikového portálu, která byla v aktuální verzi aplikace Dynamics AX nahrazena novou platformu webového klienta. |
| Nahrazeno jinou funkcí? | Nový vzor formulářů v pracovním prostoru nabízí uživatelům možnost návrhu zaměřeného na procesy, který zajišťuje snadný přístup k často používaným úkolům v rámci tohoto procesu.                       |
| Ovlivněné moduly             | Vše                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Příslušnosti k dani

|                              |                                              |
|------------------------------|----------------------------------------------|
| Důvod pro zrušení       | Málo používáno odběrateli a omezená sada funkcí. |
| Nahrazeno jinou funkcí? | Č.                                           |
| Ovlivněné moduly             | DPH v USA                                 |

### <a name="shipping-carrier-interface"></a>Rozhraní dopravce

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Duplicitní funkce                                                                                                                         |
| Nahrazeno jinou funkcí? | Ano, tato funkce byla částečně nahrazena modulem Správa přepravy, ale ještě nebyla nahrazena základním modulem Řízení skladu (WMS I). |
| Ovlivněné moduly             | Prodeje a marketing, Řízení zásob                                                                                                       |

### <a name="sites-services"></a>Služba Sites Services

Služba Sites Services umožňuje vytvářet webové stránky, které rozšiřují obchodní procesy na Internet bez IT podpory.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Infrastruktura Microsoft Azure používaná aplikací Dynamics AX má nové funkce, které lze použít (například Azure Sites). |
| Nahrazeno jinou funkcí? | Č.                                                                                                                                       |
| Ovlivněné moduly             | Nábor HR, správa případů, požadavek na cenovou nabídku, registrace dodavatele                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>Strategie prognózy poptávky SSAS

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| Důvod pro zrušení       | Návrh funkce nemůže být podporován v nové cloudové architektuře. |
| Nahrazeno jinou funkcí? | Strategie prognózy poptávky Azure Machine Learning                           |
| Ovlivněné moduly             | Plánování                                                                     |

### <a name="travel-requisitions"></a>Cestovní žádanky

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Důvod pro zrušení       | Malé využití a většina funkcí existovala v podnikovém portálu. |
| Nahrazeno jinou funkcí? | Č.                                                              |
| Ovlivněné moduly             | Správa výdajů                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Podrobnosti evidence faktur dodavatelů bez zaúčtování

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Malé využití. Tato funkce byla nahrazena deníkem faktur s funkcí workflowu. |
| Nahrazeno jinou funkcí? | Možnosti workflowu v modulu Deník faktur.                                                           |
| Ovlivněné moduly             | Závazky                                                                                        |

### <a name="virtual-company-accounts"></a>Virtuální účty společnosti

Funkce virtuálních společností není aplikací Dynamics AX již podporována. Funkce virtuálních společností umožňovala uživatelům nastavit tabulky, které mohlo sdílet více společností. Popis funkce naleznete zde: [Účty společnosti a virtuální účty společnosti](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Funkce funguje tak, že seskupuje tabulky do kolekcí, které jsou přiřazeny k virtuálním společnostem, což jsou skupiny skutečně existujících společností. Dotazy jsou vytvářeny tak, aby všechny společnosti ve virtuální společnosti měli přístup k datům v tabulkách souvisejících kolekcí tabulek.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Důvod pro zrušení</td>
<td><ul>
<li>Virtuální společnosti je nutné nastavit před uložením dat do tabulek. Zpětné začlenění virtuálních společností do existující implementace je velmi obtížné.</li>
<li>Vzhledem k tomu, že v aktuální verzi aplikace Microsoft Dynamics AX je spousta normalizací dat, je nyní těžké poznat, co přidat do kolekce tabulek. Například je obtížné poznat, které tabulky se mají sdílet. Také je nutné přidat všechny tabulky, na které je odkazováno z tabulek, které jsou ve virtuální společnosti. Kvůli normalizaci tabulky musí být i jednoduchá hlavní data, která jsou rozdělená do více tabulek, součástí virtuální společnosti. Jakákoli zde provedená chyba způsobí funkční problémy.</li>
<li>Pokud je tabulka součástí virtuální společnosti, ztratí informace o původu dat a je zaznamenána pouze virtuální společnosti.</li>
</ul></td>
</tr>
<tr class="even">
<td>Nahrazeno jinou funkcí?</td>
<td>Globální tabulky mohou být použity k zpřístupnění tabulek ze všech společností. V současné době neexistuje žádná náhrada.</td>
</tr>
<tr class="odd">
<td>Ovlivněné moduly</td>
<td>Nelze použít</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Řízení skladu II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Řešení Řízení skladu II (WMS II), které bylo k dispozici v modulu **Řízení zásob**, duplikuje funkce, které jsou v modulu **Řízení skladu** a byly vydány v aplikaci Microsoft Dynamics AX 2012 R3.                                                                         |
| Nahrazeno jinou funkcí? | Modul **Řízení skladu**, který byl vydán v aplikaci AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 a Microsoft Dynamics AX 2012 R3 CU9, nahrazuje funkce modulu Řízení skladu II. V porovnání s funkcemi modulu Řízení skladu II má nový modul více rozšířené funkce a flexibilnější procesy řízení skladu. |
| Ovlivněné moduly             | Řízení zásob, prodeje a marketing, zásobování a zdroje                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Připomenutí pracovníka v modulu Lidské zdroje

Mzdové informace lidských zdrojů

|                              |                 |
|------------------------------|-----------------|
| Důvod pro zrušení       | Malé využití       |
| Nahrazeno jinou funkcí? | Č.              |
| Ovlivněné moduly             | Lidské zdroje |

### <a name="workplanner"></a>Plánovač práce

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Malé využití                                                                                                                                                            |
| Nahrazeno jinou funkcí? | Ne, ale stránka **Vztah profilu**, kterou lze otevřít ze stránky **Skupiny profilů**, podporuje stejný obchodní scénář jako zastaralá stránka **Plánovač práce**. |
| Ovlivněné moduly             | Čas a docházka                                                                                                                                                  |

### <a name="x-financial-statements"></a>Finanční výkazy X++

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| Důvod pro zrušení       | Tato funkce byla nahrazena jinou funkcí.                                    |
| Nahrazeno jinou funkcí? | Management Reporter (v aktuální verzi aplikace Dynamics AX označena jako **Finanční výkaznictví**) |
| Ovlivněné moduly             | Hlavní kniha                                                                              |






