---
title: Kopírování odběratelů pomocí sdílených číselných řad
description: Toto téma vysvětluje, jak používat sdílené číselné řady pro kopírování odběratele do jiné právnické osoby při zachování stejného ID odběratele.
author: mikefalkner
manager: aolson
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 848c5b21afccb544e2b3d26ecc8cadac0c860796
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184133"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Kopírování odběratelů pomocí sdílených číselných řad

[!include [banner](../includes/banner.md)]

Můžete používat sdílené číselné řady pro přiřazení ID odběratelů. Sdílené číselné řady vám rovněž umožňují kopírovat odběratele z jedné právnické osoby do jiné právnické osoby při použití stejného ID odběratele v obou právnických osobách.

## <a name="setup"></a>Nastavení

Funkce je aktivována, když použijete sdílenou číselnou řadu pro přiřazení ID odběratele. Musíte použít stejnou číselnou řadu u každé právnické osoby, do které chcete odběratele kopírovat. Změnit číselnou řadu odběratele můžete na stránce **Parametry pohledávek** pro každou právnickou osobu. Zvolte **Pohledávky** \> **Parametry** a potom zvolte kartu **Číselné řady**.

Můžete rovněž nastavit číselné řady odběratelů pro každou skupinu odběratelů. Tyto číselné řady musí být rovněž sdílené. Číselná řada pro skupinu odběratelů se použije jako první. Pokud není pro skupinu odběratelů určena žádná číselná řada, použije se číselná řada určená na stránce **Parametry pohledávek**.

Pokud používáte ruční ID odběratelů, můžete rovněž kopírovat odběratele mezi právnickými osobami. Pokud se však pokusíte kopírovat odběratele do právnické osoby, kde již ID odběratele existuje, proces kopírování se nespustí.

## <a name="copy-a-customer"></a>Kopírování odběratele

Chcete-li kopírovat odběratele, zvolte **Nový** na stránce se seznamem **Všichni odběratelé** a otevřete dialogové okno **Vytvořit odběratele**. Povšimněte si, že ID nového odběratele není přiřazeno ihned. Chování se liší od chování v předchozích verzích. Protože jste ještě nezvolili skupinu odběratelů, systém nemůže určit správnou číselnou řadu, která se má použít. Navíc nemůže určit, zda se pokoušíte vytvořit nového odběratele nebo kopírovat odběratele. Proto není ID odběratele přiřazeno do té doby, než zvolíte **Uložit** ve spodní části dialogového okna.

Pokud vytváříte nového odběratele, můžete pokračovat vyplněním všech polí, jako obvykle. Po dokončení a zvolení možnosti **Uložit** uvidíte, že ID odběratele bylo přiřazeno automaticky. V případě ručních číselných řad uvidíte, že bylo použito vaše ruční ID odběratele.

Chcete-li kopírovat odběratele, zadejte v poli **Název** jeden nebo více znaků, které představují hledaného odběratele. Dialogové okno vyhledávání zobrazí seznam stran, které mohou představovat hledaného odběratele. Když vyberete jednu ze stran, na pravé straně dialogového okna se zobrazí další informace:

- Karta **Obecné** zobrazuje telefonní číslo adresu strany.
- Karta **Role** zobrazuje role, které zvolená strana může mít, a právnickou osobu, kde každou roli má.
- Karta **ID registrace daně** zobrazuje ID registrace daně, která jsou straně přiřazena.

Kopírovat stranu můžete pouze tehdy, pokud má roli odběratele, a tuto roli má v právnické osobě, která není aktuální právnickou osobou. Po nalezení strany splňující tato kritéria pokračujte podle těchto kroků.

1. Zobrazí se možnost **Kopírovat odběratele**. Ve výchozím nastavení je tato možnost nastavena na **Ne**. Chcete-li kopírovat odběratele do aktuální právnické osoby, nastavte možnost na **Ano**. 
2. Zobrazí se pole **Právnická osoba**. Vyberte právnickou osobu, ze které chcete kopírovat odběratele. Pokud odběratel existuje jen v jedné právnické osobě, je pole nastaveno ve výchozím nastavení na tuto právnickou osobu.
3. Zvolte **Zvolit**. Vytvoří se nový odběratel.

## <a name="validation"></a>Ověření

Když kopírujete odběratele, systém se pokusí uložit informace o novém odběrateli. Spustí se ověření, aby se ověřilo, že zkopírovaná data jsou správná. U každého ověření, které se nezdaří, dostanete chybovou zprávu. Chybové zprávy vysvětlují, jaké informace je třeba aktualizovat. Kopii odběratele nelze uložit, dokud neopravíte všechny chyby ověření.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Kopírování odběratele pomocí funkce vyhledávání DIČ

Můžete rovněž kopírovat odběratele pomocí funkce Vyhledávání DIČ, která je ve skupině **Registrace** na kartě **Odběratel** v podokně akcí na stránce **Všichni odběratelé**. Zobrazené dialogové okno **Vyhledávání DIČ** ukazuje DIČ, ID odběratele, název odběratele a právnickou osobu, kde se používá ID osvobození od daně. Kopírovat odběratele můžete pouze tehdy, pokud je v právnické osobě, která není aktuální právnickou osobou. Po zvolení odběratele splňujícího toto kritérium pokračujte podle těchto kroků.

1. Zobrazí se možnost **Kopírovat odběratele**. Ve výchozím nastavení je tato možnost nastavena na **Ne**. Chcete-li kopírovat odběratele do aktuální právnické osoby, nastavte možnost na **Ano**. 
2. Zvolte **Zvolit**. Vytvoří se nový odběratel.
