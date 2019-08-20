---
title: Mezipodnikové fakturování
description: Tento článek obsahuje informace a příklady o vnitropodnikové fakturaci pro projekty v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33699ea6f31651682156b4c14d3ea51285738e8a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839056"
---
# <a name="intercompany-invoicing"></a>Mezipodnikové fakturování

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace a příklady o vnitropodnikové fakturaci pro projekty v aplikaci Microsoft Dynamics 365 for Finance and Operations.

Organizace můžete mít několik divizí, dceřiných společností a ostatních právnických osob, které si navzájem předávají produkty a služby pro projekty. Právnická osoba, která poskytuje službu nebo produkt, se nazývá *půjčující právnická osoba* a právnická osoba, která přijímá službu nebo produkt, je označována jako *právnická osoba, která si půjčuje*. 

Následující obrázek znázorňuje obvyklý scénář, kde dva právní subjekty, SI FR (právnická osoba, která si půjčuje) a SI USA (půjčující právnická osoba) sdílí prostředky pro doručení projektu zákazníkovi A. V tomto scénáři má SI FR smluvně sjednáno doručení práce zákazníkovi A. 

[![Příklad mezipodnikového fakturování](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Cílem je vytvořit více flexibilní a výkonné řízení nákladů, uznání výnosů, daně a převod cen pro mezipodnikové projektové transakce. Kromě toho jsou k dispozici následující možnosti:

-   Vytvoření faktury odběratelů proti projektu právnické osoby, která si půjčuje, pomocí mezipodnikových časových rozvrhů, výdajů a faktur dodavatele v půjčující právnické osobě.
-   Podpora daňových výpočtů a nepřímých nákladů.
-   Odložení uznání výnosů v půjčující právnické osobě a doby, kdy by právnická osoba, která si půjčuje, náklady uznat.
-   Časové rozlišení výnosů nedokončené výroby (výroby NV) v půjčující právnické osobě.
-   Nastavte ceny dopravy, které mohou být založeny na různých oceňovacích modelech. Několik příkladů:
    -   **Množství** – částka, kterou zadáte v poli **Ocenění**, jsou skutečné náklady na množství nebo jednotku.
    -   **Částka nákladů** – cena/náklady na transakci plus hodnota nákladů zadaná do pole **Cena**.
    -   **Procento nákladů** – cena převodu je nákladová cena na transakci vynásobená procentem nákladů zadaných do pole **Cena**.
    -   **Procento prodejní ceny** – procento prodejní ceny, která je přenesena do půjčující právnické osoby.
    -   **Částka pod prodejní cenou** – částka, kterou právnická osoba, která si půjčuje, drží mimo prodejní ceny před převodem půjčující právnické osobě.
    -   **Příspěvkový poměr** – číslo zadané v poli **Cena** je příspěvkový poměr, který je vyjádřen jako procento prodejní ceny.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Příklad 1: Nastavení parametrů pro mezipodnikové fakturování
V tomto příkladu je USSI půjčující právnická osoba a její prostředky vykazují čas proti právnické osobě, která si půjčuje, FRSI, která vlastní smlouvu s koncovým zákazníkem. Hodiny a výdaje, které zaměstnanci USSI vykazují, mohou být součástí faktury projektu generované v FRSI. Kromě toho je třetí zdroj transakcí, který může pocházet z půjčující právnické osoby (USSI v tomto příkladu), pokud tato společnost poskytuje sdílené dodavatele dceřiným společnostem (například FRSI), a pak předá tyto náklady do projektů v rámci daných dceřiných společností. Všechny odpovídající fakturační dokumenty a daňové výpočty provádí aplikace Finance and Operations. 

V tomto příkladu musí FRSI být odběratelem právnické osoby USSI a USSI musí být dodavatelem právnické osoby FRSI. Poté je možné nastavit vnitropodnikový vztah mezi dvěma právnickými osobami. Následující postup ukazuje, jak nastavit parametry tak, aby obě právnické osoby mohly být součástí vnitropodnikové fakturace.

1. Nastavte FRSI jako zákazníka právnické osoby USSI a nastavte USSI jako dodavatele právnické osoby FRSI. Existují tři vstupní body pro kroky, které jsou požadovány pro tento úkol.

   | Krok |                                                       Vstupní bod                                                        |                                                                                                                                                                                               popis                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A.   | V rámci USSI klikněte na <strong>Pohledávky</strong> &gt; <strong>Zákazníci</strong> &gt; <strong>Všichni zákazníci</strong>. |                                                                                                                                                                  Vytvořte nový záznam zákazníka pro FRSI a vyberte skupinu odběratelů.                                                                                                                                                                  |
   |  mld.   |    V rámci FRSI klikněte na <strong>Závazky</strong> &gt; <strong>Dodavatelé</strong> &gt; <strong>Všichni dodavatelé</strong>.     |                                                                                                                                                                    Vytvořit nový záznam dodavatele pro USSI a vyberte skupinu dodavatelů.                                                                                                                                                                    |
   |  K   |                                  V FRSI otevřete záznam dodavatele, který jste právě vytvořili.                                  | Na panelu akcí na kartě <strong>Obecné</strong> ve skupině <strong>Nastavení</strong> klikněte na možnost <strong>Mezipodnikové</strong>. Na stránce <strong>Mezipodnikové</strong> na kartě <strong>Obchodní vztah</strong> nastavte jezdec <strong>Aktivní</strong> na <strong>Ano</strong>. V poli <strong>Společnost zákazníka</strong> vyberte záznam zákazníka, který jste vytvořili v kroku A. |


2. Klikněte na **Řízení projektů a účetnictví** &gt; **Nastavení** &gt; **Parametry modulu Řízení a účetnictví projektu** a potom klikněte na kartu **Mezipodnikové**. Způsob nastavení parametrů závisí na tom, zda jste právnická osoba, která si půjčuje nebo která půjčuje.
   -   Pokud jste právnická osoba, která si půjčuje, vyberte kategorii zásobování, která je používána pro párování faktur dodavatele, které jsou generovány automaticky.
   -   Pokud jste půjčující právnická osoba pro každou entitu, která si půjčuje, vyberte výchozí kategorii projektu pro každý typ transakce. Kategorie projektu se používají při konfiguraci daně, pokud fakturovaná kategorie v mezipodnikových transakcích existuje pouze u právnické osoby, která si půjčuje. Podle potřeby můžete použít časové rozlišení výnosů pro mezipodnikové transakce. Toto časové rozlišení je provedeno při zaúčtování transakcí, a poté je stornováno při zaúčtování mezipodnikové faktury.

3. Klepněte na tlačítko **Řízení a účetnictví projektu** &gt; **Nastavení** &gt; **Ceny** &gt; **Převést cenu**.
4. Vyberte měnu, typ transakce a model přenosu ceny. Měna, která je použita na faktuře, je měna, která je nakonfigurována v záznamu zákazníka pro právnickou osobu, která si půjčuje od půjčující právnické osoby. Měna je používána pro párování položek v tabulce přenosu ceny.
5. Klepněte na tlačítko **Hlavní kniha** &gt; **Nastavení účtování** &gt; **Mezipodnikové účetnictví** a nastavte vztah USSI a FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Příklad 2: Vytvoření a zaúčtování mezipodnikového časového rozvrhu
USSI – půjčující právnická osoba, musí vytvořit a odeslat časový rozvrh pro projekt z FRSI – právnické osoby, která si půjčuje. Existují dva vstupní body pro kroky, které jsou požadovány pro tento úkol.

| Krok | Vstupní bod                                                                       | popis                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A.    | **Řízení a účetnictví projektu** &gt; **Časové rozvrhy** &gt; **Všechny časové rozvrhy** | Vytvořte nový časový rozvrh. Na řádku časového rozvrhu v poli **Právnická osoba** vyberte **FRSI**. V poli **ID projektu** vyberte projekt v FRSI. Zadejte hodiny pro každý den týdne. |
| mld.    | Stránka **Časový rozvrh**                                                                | Po spuštění pracovního postupu, zaúčtujte časový rozvrh a poznamenejte si číslo dokladu.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Příklad 3: Vytvoření a zaúčtování faktury mezipodnikového dodavatele
USSI – půjčující právnická osoba, musí vytvořit a odeslat fakturu mezipodnikového dodavatele pro projekt z FRSI – právnické osoby, která si půjčuje. Tato faktura dodavatele představuje najatou lidskou sílu a výdaje, které byly dosaženy u dodavatelů, kteří jsou placeny od USSI. Existují dva vstupní body pro kroky, které jsou požadovány pro tento úkol.

| Krok | Vstupní bod                                                                                      | popis                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A.    | **Závazky** &gt; **Faktury** &gt; **Otevřít faktury dodavatele** &gt; **Nová faktura dodavatele** | Vytvořte novou fakturu dodavatele a zadejte služby, které byly pořízeny jménem projektu FRSI.                                                                                                                                                                                  |
| mld.    | Stránka **Faktura dodavatele**                                                                      | Zadejte řádky, které představují najaté služby jménem FRSI. Na pevné záložce **Podrobnosti řádku** na kartě **Projekt** na řádku faktury v poli **Projektová společnost** zadejte **FRSI**. Zadejte projekt a odpovídající informace. Poté zaúčtujte fakturu dodavatele. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Příklad 4: Vytvoření a zaúčtování mezipodnikové faktury
USSI, půjčující právnická osoba, musí vytvořit a zaúčtovat mezipodnikovou fakturu. Existují dva vstupní body pro kroky, které jsou požadovány pro tento úkol.

| Krok | Vstupní bod                                                                                             | popis                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A.    | **Řízení projektu a účetnictví** &gt; **Faktury projektu** &gt; **Mezipodniková faktura odběratele**  | Klepněte na tlačítko **Nové** a otevřete tak stránku **Vytvořit mezipodnikovou fakturu**.                                                                                  |
| mld.    | **Řízení projektu a účetnictví** &gt; **Faktury projektu** &gt; **Mezipodnikové faktury odběratele** | Na stránce **Vytvořit mezipodnikovou fakturu** zadejte právnickou osobu, určete transakci, která by měla být zahrnuta, a klepněte na tlačítko **Hledat**. |
| K    | **Řízení projektu a účetnictví** &gt; **Faktury projektu** &gt; **Mezipodnikové faktury odběratele** | Vyberte transakce, které chcete fakturovat, nebo klepnutím na tlačítko **Vybrat všechny** fakturujte všechny transakce v seznamu a klepněte na tlačítko **OK**.                  |
| P    | Stránka **Mezipodniková faktura**                                                                       | Zobrazí se návrh mezipodnikové faktury odběratele.                                                                                             |
| E.    | Stránka **Mezipodniková faktura**                                                                       | Klikněte na možnost **Zaúčtovat**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Příklad 5: Zaúčtování faktury dodavatele a faktury odběratele
Když půjčující právnická osoba, USSI, zaúčtuje fakturu mezipodnikového odběratele, vytvoří se odpovídající nevyřízená faktura dodavatele u právnické osoby, která si půjčuje – FRSI. Po zaúčtování této faktury dodavatele zaúčtuje FRSI také projektovému odběrateli hodiny zadané společností USSI. Existují tři vstupní body pro kroky, které jsou požadovány pro tento úkol.

| Krok | Vstupní bod                                                                                        | popis                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A.    | **Závazky** &gt; **Faktury** &gt; **Nevyřízené faktury dodavatele**                            | Zkontrolujte fakturu, ověřte, že jsou zahrnuty hodnoty časového rozvrhu, a poté fakturu dodavatele zaúčtujte.                  |
| mld.    | **Řízení projektu a účetnictví** &gt; **Faktury projektu** &gt; **Návrhy faktury projektu** | Vytvořte novou fakturu projektu pro projekt a ověřte, že se zobrazí hodinové transakce, které byly zaúčtovány.            |
| K    | Stránka **Projektová faktura**                                                                       | Vyberte fakturu pro projekt a potom kliknutím na tlačítko **Zobrazit podrobnosti** zkontrolujte nákladovou a prodejní částku. Nakonec fakturu zaúčtujte. |


Další informace naleznete v tématu [Konfigurace fakturování mezipodnikového projektu](tasks/configure-intercompany-project-invoicing.md).


