---
title: Definování pravidel disponibility pro položky
description: Tento postup popisuje, jak vytvořit pravidla disponibility a přepsat nastavení disponibility pro určitou položku. Také ukazuje, jak zadat výchozí nastavení skladu.
author: t-benebo
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bca0e1786adb08a7cd4795b49c974ab95183b1dd
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469304"
---
# <a name="define-coverage-rules-for-items"></a>Definování pravidel disponibility pro položky

[!include [banner](../../includes/banner.md)]

K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup popisuje, jak vytvořit pravidla disponibility a přepsat nastavení disponibility pro určitou položku. Také ukazuje, jak zadat výchozí nastavení skladu.

## <a name="create-a-coverage-group"></a>Vytvoření skupiny disponibility

Skupinu disponibility vytvoříte následujícím způsobem:

1. Přejděte na **Navigační podokno > Moduly > Hlavní plánování > Nastavení > Skupiny disponibility**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Skupina disponibility**.
1. Zadejte hodnotu do pole **Název**.
1. Zadejte hodnotu do pole **Kalendář**. Vyberte kalendář, že který se používá v hlavním plánování k vytvoření návrhu doplnění pro položky v této skupině.  
1. Vyberte možnost v poli **Kód disponibility**. Vyberte požadavek pro tento postup.  
1. V poli **Ochranná doba disponibility (ve dnech)** zadejte číslo 90. Pro položky v této skupině použijte hlavní plánování k vytvoření návrhu doplnění pro až 90 dnů v budoucnosti.  
1. V poli **Dny zpoždění** zadejte číslo 1.
1. V poli **Kladné dny** zadejte číslo 1.
1. Rozbalte nebo sbalte oddíl **Jiné**.
1. Pod částí **Pojistné doby ve dnech** v poli **Rezerva příjmu přičtená k požadovanému datu** zadejte 1. Pokud je například rezerva příjmu nastavena 1 den a řádek nákupní objednávky je naplánován na příjem dne 15. května, hlavní plánování vypočte upravené datum příjmu 16. května.
1. V poli **Rezerva výdeje odečtená od požadovaného data** zadejte číslo 1. Pokud je například pojistná doba nastavena na 1 den a řádek prodejní objednávky je naplánován na dodání 15. května, hlavní plánování vypočte upravené datum dodání 14. května.  
1. V poli **Rezerva přidaná k době realizace položky** zadejte číslo 1.
1. Zvolte možnost **Uložit**.

## <a name="create-a-new-product"></a>Vytvořit nový produkt

Nový produkt vytvoříte následujícím způsobem:

1. Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Číslo produktu**.
1. Do pole **Název produktu** zadejte hodnotu.
1. V poli **Skupina modelů položek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
1. Vyberte odkaz na vybraném řádku v seznamu.
1. V poli **Skupina položek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
1. Vyberte odkaz na vybraném řádku v seznamu.
1. V poli **Skupina dimenze úložiště** výběrem tlačítka rozevíracího seznamu otevřete vyhledávání.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
1. Vyberte odkaz na vybraném řádku v seznamu.
1. V poli **Skupina sledovací dimenze** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
1. Vyberte odkaz na vybraném řádku v seznamu.
1. Vyberte **OK**.

## <a name="set-up-default-order-settings"></a>Nastavení výchozího nastavení objednávky

Chcete-li nastavit výchozí nastavení objednávky, postupujte takto:

1. V **podokně akcí** zvolte **Plán**.
1. V části **Nastavení objednávky** vyberte **Výchozí nastavení objednávky**.
1. Do pole **Výchozí pracoviště** v možnosti **Nákupní objednávka** zadejte pracoviště, které chcete použít jako výchozí při vytvoření nákupní objednávky.
1. Do pole **Výchozí sklad** zadejte pracoviště, kde je položka uložena.
1. Rozbalte nebo sbalte oddíl **Zásoby**.
1. Do pole **Násobek** zadejte 10.
1. Do pole **Min. množství objednávky** zadejte 10.
1. Do pole **Max. množství objednávky** zadejte 100.
1. Do pole **Standardní množství objednávky** zadejte 10.
1. Do pole **Doba realizace nákupu** zadejte číslo.
1. Zaškrtněte políčko **Pracovní dny** nebo jeho zaškrtnutí zrušte.
1. Zvolte možnost **Uložit**.
1. V poli **Výchozí typ objednávky** vyberte možnost Nákupní objednávka.
1. Zvolte možnost **Uložit**.
1. Zavřete stránku. Zavřete stránku Výchozí nastavení objednávky.  

## <a name="add-an-item-to-a-coverage-group"></a>Přidání položky do skupiny disponibility

Položku do skupiny disponibility přidáte následujícím způsobem:

1. Rozbalte nebo sbalte oddíl **Plán**.
1. V poli **Skupina disponibility** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
1. V seznamu vyhledejte **skupiny disponibility**, kterou jste vytvořili.
1. Vyberte odkaz na vybraném řádku v seznamu.

## <a name="create-item-coverage-rules"></a>Vytvoření pravidel disponibility položky

Pravidla disponibility položky vytvoříte následujícím způsobem:

1. V **podokně akcí** zvolte **Plán**.
1. V části **Disponibilita** vyberte **Disponibilita položky**.
1. Zvolte **Nové**.
1. Zvolte kartu **Obecné**.
1. Zaškrtněte políčko v záhlaví nastavení **Přepsat skupinu disponibility**.
1. V poli **Ochranná doba disponibility (ve dnech)** zadejte číslo 60. I když jsou položky ve skupině disponibility Požadavky plánované 90 dnů dopředu, tato položka bude plánovaná 60 dní dopředu.  
1. V poli **Dny zpoždění** zadejte číslo 2.
1. V poli **Kladné dny** zadejte číslo 2.
1. Vyberte kartu **Doba realizace**.
1. Zaškrtněte políčko v záhlaví **Nákup**.
1. Do pole **Čas nákupu** zadejte hodnotu 5.
1. Zvolte možnost **Uložit**.

> [!NOTE]
> U vyrobených položek se **Doba realizace výroby** se používá, pokud pro položku neexistuje žádná trasa. Pokud byla k položce přidružena aktivní trasa, hlavní plánování naplánuje objednávku a vypočítá její data podle časů trasy a kapacity zdrojů (pokud je to možné).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
