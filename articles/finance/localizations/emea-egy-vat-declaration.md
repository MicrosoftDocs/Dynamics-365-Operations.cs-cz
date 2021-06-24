---
title: Přiznání k DPH pro Egypt
description: Toto téma vysvětluje, jak nakonfigurovat a vygenerovat formulář přiznání k DPH pro Egypt.
author: sndray
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9c776cedb65804f8cadbe324082c2abac435f906
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186607"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>Přiznání k DPH pro Egypt (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit a generovat formulář přiznání k DPH a knihy o prodeji a nákupu pro právnické osoby v Egyptě.

Formulář přiznání k DPH pro Egypt je oficiální dokument, který shrnuje celkovou splatnou částku DPH na výstupu, celkovou částku zpětně získané DPH na vstupu a související daňovou povinnost DPH. Formulář se používá pro všechny typy daňových poplatníků a měl by být vyplněn ručně prostřednictvím portálu daňových úřadů. Formulář přiznání k DPH se běžně označuje jako podání přiznání k DPH.

Formulář přiznání k DPH v Dynamics 365 Finance zahrnuje následující zprávy:

- Formulář 10 přiznání k DPH, který poskytuje rozpis částek, úprav a částky DPH za řádkovou položku ve formuláři přiznání k DPH, jak je popsáno v právních předpisech.
- Kniha prodejních transakcí
- Kniha nákupních transakcí

## <a name="prerequisites"></a>Předpoklady
Primární adresa právnické osoby musí být v Egyptě.
V pracovním prostoru **Správa funkcí** zapněte následující funkci:

   - (Egypt) Hierarchie kategorií pro přiznání k dani z prodeje a nákupu.

Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

V pracovním prostoru **Elektronické přiznání** importujte z úložiště následující formát elektronického hlášení:

- Přiznání k DPH Excel (EG)

> [!NOTE]
> Výše uvedený formát je založen na **Modelu daňového přiznání** a používá **Mapování modelu daňového přiznání**. Další konfigurace budou automaticky importovány.

Další informace o tom, jak importovat konfigurace elektronických sestav, najdete v části [Stažení konfigurací elektronických sestav ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Stažení konfigurací elektronického výkaznictví

Implementace formuláře přiznání k DPH pro Egypt je založena na konfiguracích elektronických přiznání (ER). Další informace o možnostech a konceptech konfigurovatelných sestav najdete v tématu [Elektronické přiznání](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Prostředí produkčního a uživatelského akceptačního testování (UAT) najdete v tématu [Stáhnout konfiguraci elektronických zpráv ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Chcete-li vygenerovat formulář přiznání k DPH a související zprávy v egyptské právnické osobě, nahrajte následující konfigurace:

- Daňové přiznání model.version.70.xml nebo novější verze
- Daňové přiznání model mapping.version.70.120.xml nebo novější verze
- Přiznání k DPH Excel (EG).version.70.32 nebo novější verze

Po stažení konfigurací ER ze služby Lifecycle Services (LCS) nebo z globálního úložiště proveďte následující kroky.

1. Přejděte do pracovního prostoru **Elektronické výkaznictví** a vyberte dlaždici **Konfigurace výkaznictví**.
1. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange** > **Načíst ze souboru XML**.
1. Nahrajte soubory v pořadí, v jakém jsou uvedeny výše. Po načtení všech konfigurací bude v aplikaci Finance uveden konfigurační strom.

## <a name="set-up-application-specific-parameters"></a>Nastavení parametrů pro konkrétní aplikaci

Parametry specifické pro aplikaci vám umožňují stanovit kritéria, jak budou daňové transakce klasifikovány a počítány v každém řádku při generování sestavy. Určení je založeno na konfiguraci skupiny DPH ze zboží, skupiny DPH, kódu DPH a dalších kritérií stanovených v definici vyhledávání.

Sestavy prodejních a nákupních knih pro Egypt obsahují sadu sloupců, které odpovídají konkrétním klasifikacím transakcí jako typů operací, produktů a dokumentů, které jsou specifické pro Egypt. Namísto zahrnutí těchto nových klasifikací jako nových vstupních údajů při zaúčtování transakcí bude klasifikace určena na základě různých vyhledávání zavedených v nabídce **Konfigurace** > **Nastavit parametry specifické pro aplikaci** > **Nastavit** za účelem splnění požadavků přiznání k DPH pro Egypt. 

![Stránka specifické parametry aplikace](media/egypt-vat-declaration-setup1.png)

Tyto následující konfigurace vyhledávání se používají ke klasifikaci transakcí v sestavách knih DPH u nákupu a prodeje:

- **PurchaseItemTypeLookup** > Sloupec O: Typ položky
- **VATRateTypeLookup** > Sloupec B: Typ daně
- **VATRateTypeLookup** > Sloupec C: Typ položky tabulky
- **PurchaseOperationTypeLookup** > Sloupec A: Typ dokumentu
- **CustomerTypeLookup** > Sloupec A: Typ dokumentu
- **SalesOperationTypeLookup** > Sloupec N: Typ operace
- **SalesItemTypeLookup** > Sloupec O: Typ položky

Pomocí následujících kroků můžete nastavit různá vyhledávání použitá ke generování přiznání k DPH a souvisejících účetních výkazů. 

1. V pracovním prostoru **Elektronické přiznání** vyberte **Konfigurace** > **Nastavení** k nastavení pravidel pro identifikaci daňové transakce v příslušném poli formuláře přiznání k DPH.
2. Vyberte aktuální verzi a na kartě s náhledem **Vyhledávání** vyberte název vyhledávání. Například **SalesItemTypeLookup**. Toto vyhledávání identifikuje seznam klasifikací v knize DPH, které jsou požadovány daňovým úřadem.
3. Na záložce s náhledem **Podmínky** vyberte **Přidat** a v novém řádku ve sloupci **Výsledek vyhledávání** vyberte související řádek, který představuje klasifikaci ve **sloupci O**.
4. Ve sloupci **Skupina DPH** vyberte skupinu DPH, která se používá k identifikaci klasifikace. Například **Domácí prodejní faktura**. Můžete také použít skupinu DPH, daňový kód nebo kombinaci atributů stromu, pokud je konfigurace definována jiným způsobem. 
5. Ve sloupci **Název** vyberte klasifikaci daňových transakcí.
6. Opakujte kroky 3–5 pro všechna dostupná vyhledávání.
7. Vyberte **Přidat** k zahrnutí závěrečného řádku záznamu a ve sloupci **Výsledek vyhledávání** vyberte **Nelze použít**. 
8. Ve zbývajících sloupcích vyberte **Není prázdné**. 
9. V poli **Stav** vyberte možnost **Dokončeno**.
10. Vyberte **Uložit** a zavřete stránku **Parametry specifické pro aplikaci**.

> [!NOTE]
> Když přidáte poslední záznam, **Nelze použít**, definujete následující pravidlo: Když skupina DPH, skupina DPH zboží, daňový kód a název, který je předán jako argument, nesplňují žádné z předchozích pravidel, transakce nejsou zahrnuty do knihy DPH. Ačkoli se toto pravidlo nepoužívá při generování sestavy, toto pravidlo pomáhá vyhnout se chybám při generování sestavy, když chybí konfigurace pravidla.

Následující tabulky představují příklad navrhované konfigurace pro popsané konfigurace vyhledávání. 

**SalesItemTypeLookup**

| Výsledek vyhledávání         | Řádek | Skupina prodejní daně    | Skupina DPH zboží    | Kód daně (kód) | Jméno                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Domácí              | 1    | VAT_LOCAL          | *Neprázdné*             | *Neprázdné*     | Prodej.                 |
| Domácí              | 2    | VAT_LOCAL          | *Neprázdné*             | *Neprázdné*     | SalesCreditNote       |
| Domácí              | 3    | VAT_FINALC         | *Neprázdné*             | *Neprázdné*     | Prodej.                 |
| Domácí              | 4    | VAT_FINALC         | *Neprázdné*             | *Neprázdné*     | SalesCreditNote       |
| Domácí              | 5    | VAT_PUBLIO         | *Neprázdné*             | *Neprázdné*     | Prodej.                 |
| Domácí              | 6    | VAT_PUBLIO         | *Neprázdné*             | *Neprázdné*     | SalesCreditNote       |
| Export                | 7    | VAT_EXPORT         | *Neprázdné*             | *Neprázdné*     | Prodej.                 |
| Export                | 8    | VAT_EXPORT         | *Neprázdné*             | *Neprázdné*     | SalesCreditNote       |
| Stroje a zařízení | 9    | *Neprázdné*        | VAT_M&E                 | *Neprázdné*     | Prodej.                 |
| Stroje a zařízení | 10   | *Neprázdné*        | VAT_M&E                 | *Neprázdné*     | SalesCreditNote       |
| Části strojů        | 11   | *Neprázdné*        | VAT_PARTS               | *Neprázdné*     | Prodej.                 |
| Části strojů        | 12   | *Neprázdné*        | VAT_PARTS               | *Neprázdné*     | SalesCreditNote       |
| Výjimky            | 13   | VAT_EXE            | *Neprázdné*           | *Neprázdné*     | SaleExempt            |
| Výjimky            | 14   | VAT_EXE            | *Neprázdné*           | *Neprázdné*     | SalesExemptCreditNote |
| Nelze použít        | 15   | *Bianko*            | *Bianko*                 | VAT_ADJ         | *Neprázdné*           |
| Nelze použít        | 16   | *Neprázdné*        | *Neprázdné*             | *Neprázdné*     | *Neprázdné*           |

 **SalesOperationTypeLookup**

| Výsledek vyhledávání  | Řádek | Skupina DPH zboží    | Kód daně    | Jméno                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Zboží          | 1    | VAT_GOODS               | *Neprázdné* | Prodej.                 |
| Zboží          | 2    | VAT_GOODS               | *Neprázdné* | SalesCreditNote       |
| Zboží          | 3    | VAT_GOODS               | *Neprázdné* | SaleExempt            |
| Zboží          | 4    | VAT_GOODS               | *Neprázdné* | SalesExemptCreditNote |
| Služby       | 5    | VAT_SERV                | *Neprázdné* | Prodej.                 |
| Služby       | 6    | VAT_SERV                | *Neprázdné* | SalesCreditNote       |
| Služby       | 7    | VAT_SERV                | *Neprázdné* | SaleExempt            |
| Služby       | 8    | VAT_SERV                | *Neprázdné* | SalesExemptCreditNote |
| Úpravy    | 9    | *Bianko*                 | VAT_ADJ     | Prodej.                 |
| Úpravy    | 10   | *Bianko*                 | VAT_ADJ     | SalesCreditNote       |
| Nelze použít | 11   | *Neprázdné*             | *Neprázdné* | *Neprázdné*           |

**PurchaseItemTypeLookup**

| Výsledek vyhledávání          | Řádek | Skupina DPH zboží    | Kód daně    | Jméno                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Zboží                  | 1    | VAT_GOODS               | *Neprázdné* | Nákup                 |
| Zboží                  | 2    | VAT_GOODS               | *Neprázdné* | PurchaseCreditNote       |
| Služby               | 3    | VAT_SERV                | *Neprázdné* | Nákup                 |
| Služby               | 4    | VAT_SERV                | *Neprázdné* | PurchaseCreditNote       |
| Stroje a zařízení  | 5    | VAT_M&E                 | *Neprázdné* | Nákup                 |
| Stroje a zařízení  | 6    | VAT_M&E                 | *Neprázdné* | PurchaseCreditNote       |
| Části strojů         | 7    | VAT_PARTS               | *Neprázdné* | Nákup                 |
| Části strojů         | 8    | VAT_PARTS               | *Neprázdné* | PurchaseCreditNote       |
| Výjimky             | 9    | VAT_EXE                 | *Není banka*  | PurchaseExempt           |
| Výjimky             | 10   | VAT_EXE                 | *Neprázdné* | PurchaseExemptCreditNote |
| Nelze použít         | 11   | *Neprázdné*             | *Neprázdné* | *Neprázdné*              |

**PurchaseOperationTypeLookup**

| Výsledek vyhledávání  | Řádek | Skupina prodejní daně  | Kód daně    | Jméno                     |
|----------------|------|------------------|-------------|--------------------------|
| Domácí       | 1    | VAT_LOCAL        | *Neprázdné* | Nákup                 |
| Domácí       | 2    | VAT_LOCAL        | *Neprázdné* | PurchaseCreditNote       |
| Domácí       | 3    | VAT_LOCAL        | *Neprázdné* | PurchaseExempt           |
| Domácí       | 4    | VAT_LOCAL        | *Neprázdné* | PurchaseExemptCreditNote |
| Importováno       | 5    | VAT_IMPORT       | *Neprázdné* | Nákup                 |
| Importováno       | 6    | VAT_IMPORT       | *Neprázdné* | PurchaseCreditNote       |
| Importováno       | 7    | VAT_IMPORT       | *Neprázdné* | PurchaseExempt           |
| Importováno       | 8    | VAT_IMPORT       | *Neprázdné* | PurchaseExemptCreditNote |
| Úpravy    | 9    | *Bianko*          | VAT_ADJ     | PurchaseCreditNote       |
| Úpravy    | 10   | *Bianko*          | VAT_ADJ     | Nákup                 |
| Nelze použít | 11   | *Neprázdné*      | *Neprázdné* | *Neprázdné*              |

**CustomerTypeLookup**

|    Výsledek vyhledávání    | Řádek | Skupina prodejní daně |
|---------------------|------|-----------------|
| Organizace        |  1   | VAT_LOCAL       |
| Organizace        |  2   | VAT_EXPORT      |
| Organizace        |  3   | VAT_EXE         |
| Konečný spotřebitel      |  4   | VAT_FINALC      |
| Veřejná organizace |  5   | VAT_PUBLIO      |
| Nelze použít.      |  6   | *Neprázdné*     |

**VATRateTypeLookup**

| Výsledek vyhledávání  | Řádek | Kód daně (kód) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Neprázdné*     |
| SecondTable    | 4    | *Neprázdné*     |
| Nelze použít | 5    | *Neprázdné*     |


## <a name="set-up-general-ledger-parameters"></a>Nastavení parametrů hlavní knihy

Chcete-li vygenerovat hlášení z daňového přiznání k DPH ve formátu Microsoft Excel, definujte formát ER na stránce **Obecné parametry hlavní knihy**.

1. Přejděte na **Daň** > **Nastavení** > **Parametry hlavní knihy**.
2. Na kartě **DPH** v části **Možnosti daně** v poli **Mapování formátu přiznání k DPH** vyberte **Přiznání k DPH pro Excel (EG)**. Pokud toto pole necháte prázdné, vygeneruje se standardní hlášení o DPH ve formátu SSRS.
3. Vyberte **Hierarchie kategorií**. Tato kategorie aktivuje kód zboží v transakcích na kartě Zahraniční obchod a umožňuje uživatelům vybrat a klasifikovat zboží a služby. Popis této klasifikace je podrobně uveden ve zprávách o prodejních a nákupních transakcích. Tato konfigurace je volitelná.

![Formulář přiznání](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>Vygenerovat sestavu přiznání k DPH
Proces přípravy a odeslání sestavu přiznání k DPH za období je založen na transakcích platby DPH, které byly zaúčtovány během úlohy Vypořádat a zaúčtovat DPH. Další informace o vypořádání a vykazování DPH naleznete v tématu [Přehled DPH](../general-ledger/indirect-taxes-overview.md).

Chcete-li vygenerovat zprávu o daňovém přiznání, proveďte následující kroky.

1. Přejděte do nabídky **Daň** > **Přiznání** > **DPH** > **Přiznat DPH za zúčtovací období** nebo **Vypořádat a zaúčtovat DPH**.
2. Vyberte **Zúčtovací období**.
3. Vyberte datum od a poté vyberte verzi platby DPH.
5. Vyberte **OK**. 
6. Zadejte částku kreditu z předchozího období, pokud je to možné, nebo ponechejte částku nulovou.
7. V poli **Detaily výkazů** vyberte jednu z následujících dostupných možností. 
   - **Kniha DPH na vstupu**: Vygenerovat sestavu s podrobnostmi transakcí daně na vstupu.
   - **Kniha DPH na výstupu**: Vygenerovat sestavu s podrobnostmi transakcí daně na výstupu.
   - **Přiznání k DPH**: Vygenerovat pouze formulář pro přiznání k DPH.
8. Zadejte jméno osoby, která je zaregistrována pro přiřazení formuláře.
9. Vyberte jazyk. Všechny sestavy jsou přeloženy do **en-us** a **ar-eg**.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


