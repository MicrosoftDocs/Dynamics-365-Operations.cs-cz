---
title: Kopírování dodavatelů pomocí sdílených číselných řad
description: Toto téma vysvětluje, jak používat sdílené číselné řady pro kopírování dodavatele do jiné právnické osoby při zachování stejného ID dodavatele.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e777596e1bd752db438fc3591ce1125a301f4097
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836941"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Kopírování dodavatelů pomocí sdílených číselných řad

[!include [banner](../includes/banner.md)]

Můžete používat sdílené číselné řady pro přiřazení ID dodavatelů. Sdílené číselné řady vám rovněž umožňují kopírovat dodavatele z jedné právnické osoby do jiné právnické osoby při použití stejného ID dodavatele v obou právnických osobách.

## <a name="setup"></a>Nastavení

Funkce je aktivována, když použijete sdílenou číselnou řadu pro přiřazení ID dodavatele. Musíte použít stejnou číselnou řadu u každé právnické osoby, do které chcete dodavatele kopírovat. Změnit číselnou řadu dodavatele můžete na stránce **Parametry závazků** pro každou právnickou osobu. Zvolte **Závazky** \> **Nastavení** \> **Parametry závazků** a potom zvolte kartu **Číselné řady**.

Můžete rovněž nastavit číselné řady dodavatelů pro každou skupinu dodavatelů. Tyto číselné řady musí být rovněž sdílené. Číselná řada pro skupinu dodavatelů se použije jako první. Pokud není pro skupinu dodavatelů určena žádná číselná řada, použije se číselná řada určená na stránce **Parametry závazků**.

Pokud používáte ruční ID dodavatelů, můžete rovněž kopírovat dodavatele mezi právnickými osobami. Pokud se však pokusíte kopírovat dodavatele do právnické osoby, kde již ID dodavatele existuje, proces kopírování se nespustí.

## <a name="copy-a-vendor"></a>Kopírovat dodavatele

Chcete-li kopírovat dodavatele, zvolte **Nový** na stránce se seznamem **Všichni dodavatelé**  a otevřete stránku **Všichni dodavatelé, nový záznam**. Povšimněte si, že ID nového dodavatele není přiřazeno ihned. Chování se liší od chování v předchozích verzích aplikace Microsoft Dynamics 365 for Finance and Operations. Protože jste ještě nezvolili skupinu dodavatelů, systém nemůže určit správnou číselnou řadu, která se má použít. Navíc nemůže určit, zda se pokoušíte vytvořit nového dodavatele nebo kopírovat dodavatele. Proto není ID dodavatele přiřazeno do té doby, než zvolíte **Uložit** ve spodní části stránky.

Pokud vytváříte nového dodavatele, můžete pokračovat vyplněním všech polí, jako obvykle. Po dokončení a zvolení možnosti **Uložit** uvidíte, že ID dodavatele bylo přiřazeno automaticky. V případě ručních číselných řad uvidíte, že bylo použito vaše ruční ID dodavatele.

Chcete-li kopírovat dodavatele, zadejte v poli **Název** jeden nebo více znaků, které představují hledaného dodavatele. Dialogové okno vyhledávání zobrazí seznam stran, které mohou představovat hledaného dodavatele. Když vyberete jednu ze stran, na pravé straně dialogového okna se zobrazí další informace:

- Karta **Obecné** zobrazuje telefonní číslo adresu strany.
- Karta **Role** zobrazuje role, které zvolená strana může mít, a právnickou osobu, kde každou roli má.
- Karta **ID registrace daně** zobrazuje ID registrace daně, která jsou straně přiřazena.

Kopírovat stranu můžete pouze tehdy, pokud má roli dodavatele, a tuto roli má v právnické osobě, která není aktuální právnickou osobou. Po nalezení strany splňující tato kritéria pokračujte podle těchto kroků.

1. Zobrazí se možnost **Kopírovat dodavatele**. Ve výchozím nastavení je tato možnost nastavena na **Ne**. Chcete-li kopírovat dodavatele do aktuální právnické osoby, nastavte možnost na **Ano**. 
2. Zobrazí se pole **Právnická osoba**. Vyberte právnickou osobu, ze které chcete kopírovat dodavatele. Pokud dodavatel existuje jen v jedné právnické osobě, je pole nastaveno ve výchozím nastavení na tuto právnickou osobu.
3. Zvolte **Zvolit**. Vytvoří se nový dodavatel.

## <a name="validation"></a>Ověření

Když kopírujete dodavatele, systém se pokusí uložit informace o novém dodavateli. Spustí se ověření, aby se ověřilo, že zkopírovaná data jsou správná. U každého ověření, které se nezdaří, dostanete chybovou zprávu. Chybové zprávy vysvětlují, jaké informace je třeba aktualizovat. Kopii dodavatele nelze uložit, dokud neopravíte všechny chyby ověření.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Kopírování dodavatele pomocí funkce Vyhledávání DIČ

Můžete rovněž kopírovat dodavatele pomocí funkce Vyhledávání DIČ, která je ve skupině **Registrace** na kartě **Dodavatel** v podokně akcí na stránce **Všichni dodavatelé**. Zobrazené dialogové okno **Vyhledávání DIČ** ukazuje DIČ, ID dodavatele, název dodavatele a právnickou osobu, kde se používá ID osvobození od daně. Kopírovat dodavatele můžete pouze tehdy, pokud je v právnické osobě, která není aktuální právnickou osobou. Po zvolení dodavatele splňujícího toto kritérium pokračujte podle těchto kroků.

1. Zobrazí se možnost **Kopírovat dodavatele**. Ve výchozím nastavení je tato možnost nastavena na **Ne**. Chcete-li kopírovat dodavatele do aktuální právnické osoby, nastavte možnost na **Ano**.
2. Zvolte **Zvolit**. Vytvoří se nový dodavatel.
