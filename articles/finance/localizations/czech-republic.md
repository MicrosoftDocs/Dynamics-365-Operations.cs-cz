---
title: Přehled – Česká republika
description: Toto téma poskytuje přehled o funkci aplikace Dynamics 365 Finance, která je specifická pro Českou republiku.
author: ShylaThompson
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic
ms.author: roschlom
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a2fa093e8a24b68074a1c843049999131823c2a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217344"
---
# <a name="czech-republic-overview"></a>Přehled – Česká republika

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace a odkazy na zdroje, které vám pomohou nastavit aplikaci pro právnické osoby s primární adresou v České republice.

## <a name="fixed-assets"></a>Dlouhodobý majetek
Následující témata poskytují informace týkající se dlouhodobého majetku v České republice:

-   [Zaokrouhlení odpisování](emea-cze-depreciation-rounding.md)
-   [Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku](emea-cze-half-depreciation-fixed-asset-disposal.md)
-   [Přerušení odpisování (svátky)](emea-cze-depreciation-suspension-holidays.md)
-   [Metody odpisování dlouhodobého majetku pro Českou republiku](emea-cze-fixed-assets-depreciation.md)
-   [Zaúčtování předpořízení dlouhodobého majetku](emea-pre-acquisition-acquisition-fixed-asset.md)

## <a name="vat-reporting"></a>Vykazování DPH
Informace o nastavení a generování výkazu DPH pro právnické osoby, které jsou umístěny v České republice, naleznete v tématu [Výkaz DPH pro Českou republiku](emea-cze-vat-statement-details.md). Informace o přiznání k DPH viz [Přiznání k DPH (Česká republika)](emea-cze-vat-declaration-tax-declaration-model.md)

### <a name="intra-community-vat"></a>DPH intrakomunitárního plnění
Tato část uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku. 

Když právnické osoby, které mají primární adresu v České republice, nakupují od členských států Evropské unie (EU), měly by provést vlastní vyměření DPH, aby se zajistilo, že jsou splněny následující podmínky:

-   DPH na výstupu se platí v období DPH, kdy byla vystavena faktura (datum dokumentu).
-   DPH na vstupu nebyla odečtena před přijetím dokumentu (datum rejstříku DPH).

Informace o intrakomunitární DPH mohou být vypočteny a zaúčtovány automaticky. Při zaúčtování faktury dodavatele v Evropské unii (EU) jsou vytvořeny dvě transakce DPH ve stejné výši. Jedna transakce DPH je vytvořena pro závazek prodejní daně a druhá pro pohledávku prodejní daně. Aby se tento požadavek projevil, je třeba nastavit následující položky:

-   Zaškrtněte políčko **DPH intrakomunitárního plnění** na stránce **Parametry závazků** (**Závazky** > **Nastavení** > **Parametry závazků**).
-   Zaškrtněte políčko **Datum dokumentu pro intrakomunitární DPH** na stránce **Parametry závazků**.
-   Vytvořte dva kódy daně z prodeje: jeden, který má kladné procento daně z prodeje a druhý, který má záporné procento daně z prodeje.
-   Vytvořte skupinu daně z prodeje obsahující kladné i záporné kódy daně z prodeje. Pro záporný kód daně z prodeje vyberte parametr **DPH intrakomunitárního plnění**.
-   V denících vyberte parametr **Datum dokumentu pro intrakomunitární DPH**.

Při zaúčtování nákupní faktury, pohledávka DPH a závazek DPH jsou účtovány ve stejnou dobu. V případě kladných transakcí daně z prodeje je datum registru DPH nastaveno na datum registru DPH ze stránky zaúčtování faktury a směrování daně z prodeje je **DPH na vstupu**. V případě záporných transakcí daně z prodeje je datum registru DPH nastaveno na datum dokumentu a směrování daně z prodeje je **DPH na výstupu**.

## <a name="credit-note-on-cash-discount"></a>Dobropis na platební slevu
Informace o vytváření, zaúčtování a tisku dobropisů pro hotovostní slevy, které jsou přiřazeny odběratelům, naleznete v tématu [Dobropis na platební slevu](emea-cze-credit-note-cash-discount.md).

## <a name="split-periods-in-periodic-journals"></a>Rozdělení období v periodických denících
Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku je stránka **Periodické deníky** rozšířena o funkci rozdělení na období. Další informace naleznete v jednom z následujících témat:
- [Rozdělení období v periodických denících](emea-create-post-periodic-journals.md)
- [Účtování periodických deníků](../general-ledger/tasks/post-periodic-journals.md)

## <a name="signers-for-print-forms"></a>Podepisující uživatelé tištěných formulářů
Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku můžete nastavit podepisující osoby a tituly pro odběratele a dodavatele, kteří tisknou dokumenty, jako jsou faktury a platební příkazy. Další informace naleznete v tématu [Nastavení podepisujících formulářů pro tisk](emea-set-up-signers-for-printing-forms.md).

## <a name="customize-currency-units-and-subunits"></a>Přizpůsobení jednotek a dílčích jednotek měny
Můžete aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko. Můžete nastavit úplný a krátký název pro měnové jednotky a podjednotky. Další informace viz [Aktualizace způsobu zobrazování částek v sestavách a dokumentech](emea-amount-printing-forms.md)

> [!NOTE]
> Prodejní daň v místní měně můžete prohlížet v sestavě **Deník faktur odběratele** a sestavě **Deník faktur dodavatele**.

## <a name="specify-bank-symbols-for-bank-accounts"></a> Určete symboly banky pro bankovní účty 
Konstantní symboly jsou přiřazeny bankovním účtům a použity v prodejních objednávkách, nákupních objednávkách, na fakturách odběratelů a volných fakturách. Pomocí stránky **Bankovní konstatní symboly** můžete nastavit seznam konstantních symbolů. Ve výchozím nastavení, pokud nastavíte konstantní symbol pro konkrétní bankovní účet společnosti, bude symbol zkopírován do prodejních objednávek a volného textu. Z prodejní objednávky nebo volného textu faktury je konstantní symbol převeden do faktury odběratele. 
> [!NOTE]
> Ve výchozím nastavení, pokud nastavíte specifický symbol pro bankovní účet, je zkopírován do výtisku formuláře faktury dodavatele. Konstantní symbol je také zobrazen na výtiscích faktur. 

Bankovní symboly můžete nastavit na stránce **Bankovní konstantní symboly** (**Pokladna a banka** > **Nastavení** > **Konstantní symboly**). 

## <a name="year-end-close"></a>Roční uzávěrka
Existují jedinečné aspekty procesu roční uzávěrky a počátečních transakcí pro Českou republiku. Proces roční uzávěrky můžete nastavit následujícím způsobem: 
- Účtování do různých účtů pro uzavření a otevření rozvahových účtů. 
- Převod ročního výsledku zisků nebo ztrát do nově otevřeného roku na jiný účet.
Další informace naleznete v tématu [roční uzávěrka pro Českou republiku a Maďarsko](emea-cze-hun-year-end.md).

## <a name="additional-resources"></a>Další prostředky
- [Portál lokalizace Microsoft Dynamics: Sestava České republiky](https://mbs.microsoft.com/files/customer/AX/Support/supportnews/CzechRepublic.html)
- [Přehled elektronického výkaznictví](../../dev-itpro/analytics/general-electronic-reporting.md)
- [Stažení konfigurací elektronického výkaznictví ze služby Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]