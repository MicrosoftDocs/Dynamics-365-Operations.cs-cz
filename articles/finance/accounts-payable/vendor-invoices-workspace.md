---
title: Pracovní prostor pro zadávání faktur dodavatele
description: Toto téma vysvětluje, jak nastavit pracovní prostor, který souvisí s fakturami dodavatelů a který zobrazuje informace, které jsou k dispozici prostřednictvím Microsoft Power BI.
author: abruer
manager: AnnBe
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a4ba676d9b6df69cf0a91862bcc4d2837b7cb69e
ms.sourcegitcommit: 0efa93f11847a2b75d13cd0a49e716c76130ec44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2020
ms.locfileid: "4441316"
---
# <a name="vendor-invoice-entry-workspace"></a>Pracovní prostor pro zadávání faktur dodavatele

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak nastavit pracovní prostor, který souvisí s fakturami dodavatelů a který zobrazuje informace, které jsou k dispozici prostřednictvím Microsoft Power BI. Informace o faktuře dodavatele v tomto pracovním prostoru jsou filtrovány pro konkrétní uživatele a jsou zobrazeny v grafickém formátu.

## <a name="overview"></a>Přehled

Pracovní prostor **Záznam faktury dodavatele** zobrazuje informace související se zpracováním faktur dodavatele. Tento pracovní prostor obsahuje zobrazení **Moje práce** a stránku **Analýza – všechny společnosti**. Zobrazení **Moje práce** zobrazuje souhrnné dlaždice, mřížky transakce dodavatele a související informace o dodavateli. Stránka **Analýza – všechny společnosti** používá funkce Power BI k zobrazení vizualizací, které se vztahují k fakturám dodavatelů.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Nastavení pracovního prostoru, aby zobrazoval obsah Power BI

Toto nastavení musíte provést, než budou moci být zobrazena data ve vizualizacích Power BI v pracovním prostoru **Záznam faktury dodavatele**.

1. V pracovním prostoru **Správa funkcí** filtrováním seznamu vyhledejte funkci **Automatizace faktur dodavatele**.
3. Vyberte **Povolit**.
4. Chcete-li zajistit, aby faktury mohly být zpracovány od začátku do konce bez nutnosti ručního zásahu, nastavte workflow faktur dodavatele. Pracovní postup nastavíte tak, že přejděte na **Závazky \> Nastavení \> Workflowy závazků**.
5. Přejděte na **Závazky \> Nastavení \> Parametry závazků** a vyberte kartu **Automatizace faktur dodavatele**. Další informace viz [Možnosti nastavení pro automatizaci faktur dodavatele](vnd-invoice-set-up-options.md).
6. Nastavte možnost **Automaticky odesílat importované faktury do workflow** na **Ano**.
7. Pokud by se příjemkami produktů měly automaticky shodovat, nastavte možnost **Automaticky přiřadit příjemky produktů k řádkům faktur** na **Ano**.
8. Zkontrolujte zbývající volitelná nastavení a nakonfigurujte je podle požadavků vaší organizace.
9. Přejděte na **Správa systému \> Nastavení \> Systémové parametry** a nastavte pole **Měna systému** a **Směnný kurz systému**.
10. Přejděte na **Hlavní kniha \> Nastavení \> Účetní kniha** a nastavte pole **Měna účtování** a **Typ směnného kurzu**.
11. Přejděte na **Hlavní kniha \> Měny \> Směnné kurzy měn** a zadejte směnné kurzy mezi měnou transakce a zúčtovací měnou a mezi zúčtovací měnou a měnou systému.
12. Přejděte na **Správa systému \> Nastavení \> Úložiště entit** a vyhledejte **Měření automatizace faktur dodavatele**. Vyberte **Aktualizovat**.

Chcete-li zobrazit informace, které se zobrazily v pracovním prostoru, musíte mít roli zabezpečení Manažer závazků nebo Úředník závazků.

## <a name="my-work-view"></a>Zobrazení Moje práce

### <a name="company-selection"></a>Výběr společnosti

Když je zapnutá funkce **Automatizovat faktury dodavatele**, pole **Společnost** se objeví v horní části pracovního prostoru. Výběr pole **Společnost** ovlivňuje všechny informace zobrazené v pracovním prostoru. Ve výchozím nastavení zobrazení obsahuje informace o společnosti, ke které jste se přihlásili. Výběrem jiné společnosti v poli **Společnost** můžete zobrazit informace o této společnosti v pracovním prostoru. Poté můžete vybrat dlaždici v pracovním prostoru a přejít na související stránku ve vybrané společnosti.

### <a name="summary-tiles"></a>Dlaždice souhrnu

Dlaždice v sekci **Souhrn nevyřízených faktur** v zobrazení **Moje práce** poskytují přehled o stavu faktur dodavatele. Můžete zobrazit deníky, které ještě nejsou zaúčtovány, a faktury, které jsou pozastaveny. Kromě toho existují čtyři dlaždice, které jsou přidruženy k funkci automatizace faktur dodavatele:

- Je nutné ruční párování příjemky
- Ověření párování nebylo úspěšné
- Faktury neodeslané do pracovního postupu
- Faktury nebyly importovány

(Tyto čtyři dlaždice vyžadují, aby byla ve správě funkcí zapnuta funkce Automatizace faktur dodavatele.)

Chcete-li použít dlaždici **Obnovit faktury dodavatele**, tato funkce musí být zapnutá v části Parametry závazků. Jděte na **Závazky \> Parametry závazků** a poté na kartě **Faktura** nastavte možnost **Povolit obnovení faktury dodavatele** na **Ano**.

Když je funkce zapnutá, v pracovním prostoru v sekci **Deníky** budou také seskupeny tři dlaždice. Dlaždice jsou pojmenovány **Deníky**, **Deníky – přiděleno mně** a **Evidence faktur**. 

Informace v sekci **Souhrn nevyřízených faktur** platí pro společnost, která je nastavena jako výchozí společnost pro vaše přihlášení.

### <a name="creating-new-records"></a>Vytvoření nových záznamů

Chcete-li vytvořit nový záznam faktury, vyberte **Nový** a potom vyberte jeden z následujících typů záznamů v seznamu:

- Faktury dodavatele
- Deník faktur
- Globální deník faktur
- Registr faktur
- Schválení faktury

Všimněte si, že záznam, který vytvoříte, je založen na filtru společnosti, nikoli na společnosti, ke které jste přihlášeni. Například jste přihlášeni ke společnosti **UMSF**, ale filtr společnosti je nastaven na **GBSI**. V tomto případě, když vyberete **Nový** a poté v seznamu vyberete typ záznamu, záznam se vytvoří ve společnosti GBSI.

### <a name="documents-not-invoiced-grids"></a>Mřížky nefakturovaných dokumentů

Sekce **Nefakturované dokumenty** obsahuje mřížky, které zobrazují dokumenty, které čekají na faktury dodavatele.

Mřížka **Otevřené nákupní objednávky** obsahuje všechny nákupní objednávky, které ještě nejsou plně fakturovány. Můžete použít tlačítko **Fakturovat** pro vytvoření faktury dodavatele pro nákupní objednávku. Můžete použít tlačítko **Zálohová faktura** pro vytvoření zálohové faktury pro nákupní objednávku.

Mřížka **Příjemky produktu** obsahuje všechny transakce nákupních příjemek, které ještě nejsou plně fakturovány. Můžete použít tlačítko **Fakturovat** pro vytvoření faktury dodavatele pro nákupní objednávku.

Mřížka **Nevyřízené faktury dodavatele** obsahuje všechny faktury dodavatele, které nebyly odeslány do systému workflow. Můžete použít pole **Vyhledávání** nebo filtr společnosti k vyhledání konkrétní faktury dodavatele. Můžete použít tlačítko **Upravit** pro úpravu transakce, která se objeví v mřížce.

V mřížce **Hledání nákupní objednávky** můžete použít pole **Vyhledávání** pro vyhledání konkrétní nákupní objednávky.

### <a name="related-information"></a>Související informace

Informace o zaúčtovaných fakturách můžete zobrazit pomocí odkazů na pravé straně pracovního prostoru. Mezi tyto odkazy patří **Otevřené faktury dodavatele**, **Deník faktur** a **Historie faktur a podrobnosti párování**. V sekci **Prodejci** můžete přistupovat k filtrovanému seznamu, který obsahuje všechny pozastavené dodavatele, nebo můžete použít odkaz **Všichni prodejci**. Dostupné jsou také odkazy **Všechny nákupní objednávky** a **Otevřené zálohy**.

### <a name="analytics--all-companies-page"></a>Stránka Analýza – všechny společnosti

Když je možnost **Automaticky odesílat importované faktury do workflow** nastavena na **Ano** na stránce **Parametry závazků**, můžete si prohlédnout analýzy automatizace. Stránka **Analýza – všechny společnosti** poskytuje důležité metriky, například faktury dodavatele, které schvaluje schvalovatel a společnost. Tato stránka obsahuje pět stránek sestavy. Jedna stránka obsahuje přehled a další stránky poskytují podrobné informace o metrikách automatizace závazků.

V následující tabulce jsou uvedeny vizualizace dostupné na stránkách sestav.

| Stránka sestavy                    | Vizualizace |
|--------------------------------|----------------|
| Přehled faktury dodavatele        | <ul><li>Nevyřízené faktury dodavatele v automatizaci v systémové měně</li><li>Faktury, které se nepodařilo importovat</li><li>Faktury ve workflow</li><li>Bezdotykové faktury za posledních 30 dní</li><li>Celkové automatizované faktury za posledních 30 dní</li><li>Zůstatek otevřených faktur v systémové měně</li><li>Důvody selhání za posledních 30 dní</li><li>Procento zaúčtovaných faktur, které byly zpracovány automaticky</li><li>Dny na zpracování faktury</ul></li> |
| Stav automatizace              | <ul><li>Bezdotykové faktury za posledních 30 dní</li><li>Bezdotykové faktury za posledních 30 dní podle společnosti</li><li>Bezdotykové faktury za posledních 30 dní skupiny dodavatele</li><li>Procento zaúčtovaných faktur, které byly zpracovány automaticky</li><li>Dny na zpracování faktury</li></ul> |
| Faktury, které se nepodařilo importovat | <ul><li>Faktury, které se nepodařilo importovat</li><li>Faktury, které se nepodařilo importovat, podle společnosti</li></ul> |
| Důvody selhání automatizace | <ul><li>Faktury, které selhaly</li><li>Faktury, které selhaly podle společnosti</li><li>Faktury, které selhaly, podle skupiny dodavatele</li></ul> |
| Stav pracovního postupu                | <ul><li>Faktury ve workflow</li><li>Instance workflowu faktury dodavatele</li><li>Přiřazení na schvalovatele</li><li>Workflow faktury dodavatele na společnost</li><li>Průměrný počet dnů ve workflowu podle schvalujícího</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]