---
title: Stavy životního cyklu požadavku na údržbu
description: Toto téma popisuje, jak nastavit stavy životního cyklu požadavků na údržbu v modulu Správa majetku.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b54b58a29dc23e19f5065363c331351f24267ac
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360939"
---
# <a name="maintenance-request-lifecycle-states"></a>Stavy životního cyklu požadavku na údržbu

[!include [banner](../../includes/banner.md)]

 


Stavy životního cyklu požadavků údržby definují fáze, kterými může požadavek projít. Příklady zahrnují **Vytvořené**, **Aktivní** a **Ukončené**. Když je požadavek na údržbu převeden na pracovní příkaz, stav životního cyklu požadavku údržby by měl být aktualizován na **Ukončený** nebo **Uzavřený**, aby bylo možné označit, že požadavek na údržbu již není aktivní. Na stránce seznamu **Všechny požadavky na údržbu** můžete vidět všechny požadavky na údržbu bez ohledu na jejich stav životního cyklu.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Nastavit stavy životního cyklu požadavku na údržbu

1. Vyberte **Správa majetku**\>**Nastavení**\> **Požadavky na údržbu** \>**Stavy životního cyklu**.
2. Zvolte **Nový** pro vytvoření stavu životního cyklu požadavku na údržbu.
3. Do pole **Stav životního cyklu** zadejte ID stavu životního cyklu.
4. Do pole **Název** zadejte název.

    Na kartě **Podrobnosti** pole **Modely životního cyklu** zobrazuje počet modelů životního cyklu požadavku na údržbu, které používají tento stav životního cyklu.

5. Na záložce **Obecné** nastavte možnost **Aktivní** na **Ano**, pokud by požadavek údržby měl být aktivní v době, kdy je v tomto stavu životního cyklu.
6. Nastavte možnost **Nastavit skutečné ukončení** na **Ano**, pokud má být skutečné koncové datum a čas automaticky zadáno do požadavku údržby, který je v tomto stavu životního cyklu.
7. Možnost **Vytvořit pracovní příkaz** nastavte na **Ano**, pokud lze pracovní příkaz vytvořit z požadavku na údržbu, který je v tomto stavu životního cyklu.
8. Možnost **Odstranit** nastavte na **Ano**, pokud lze požadavek na údržbu odstranit v době, kdy je v tomto stavu životního cyklu.
9. Na pevné záložce **Aktualizace** jsou možnosti **Vstupní** a **Výstupní** v části **Majetek** relevantní, pokud použijete opravu skladu. Nastavte příslušnou možnost na hodnotu **Ano** v případě, že stav životního cyklu majetku vybraného v požadavku na údržbu by měl být automaticky aktualizován na **Příchozí** nebo **Odchozí**, pokud je stav cyklu životnosti požadavku na údržbu nastaven na **Příchozí** nebo **Odchozí**.

Následující ilustrace znázorňuje příklad stránky **Stavy životního cyklu požadavků na údržbu**.

![Stránka Stavy životního cyklu požadavku na údržbu.](media/02-setup-for-requests.png)

> [!NOTE]
> Stavy životního cyklu požadavků na údržbu, skupiny stavů životního cyklu a typy jsou propojeny a používány stejným způsobem jako stavy životního cyklu pracovních příkazů, skupiny stavů životního cyklu a typy. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Nastavit modely životního cyklu požadavku na údržbu

Po vytvoření stavů životního cyklu, které jsou požadovány pro vaše požadavky na údržbu, je lze rozdělit do skupin stavů životního cyklu nebo do modelů životního cyklu. Modely životního cyklu požadavků na údržbu slouží k vytvoření toku, který lze použít pro různé typy požadavků na údržbu. Je třeba vytvořit minimálně jeden standardní model životního cyklu požadavků na údržbu.

1. Vyberte **Správa majetku**\>**Nastavení**\> **Požadavky na údržbu** \>**Modely životního cyklu**.
2. Zvolte **Nový** pro vytvoření modelu životního cyklu požadavku na údržbu.
3. Do pole **Model životního cyklu** zadejte ID modelu životního cyklu.
4. Do pole **Název** zadejte název.

    Na kartě **Podrobnosti** ukazuje položka **Stavy životního cyklu** počet stavů životního cyklu, které jsou vybrány v tomto modelu životního cyklu majetku. Pole **Typy požadavků na údržbu** zobrazuje počet typů požadavků na údržbu, které používají tento model životního cyklu.

5. Na kartě **Stavy životního cyklu** vyberte stavy životního cyklu, které si přejete zahrnout v modelu životního cyklu:

    - Chcete-li v modelu životního cyklu použít stav životního cyklu, vyberte jej v části **Zbývající stavy životního cyklu** a potom vyberte tlačítko šipky vpravo ![Šipka vpravo](media/03-setup-for-requests.png) a přesuňte jej do části Vybrané stavy životního cyklu. pro přesun do části **Vybrané stavy životního cyklu**.
    - Chcete-li do modelu životního cyklu zahrnout všechny dostupné stavy životního cyklu, vyberte tlačítko **Vybrat všechny dostupné stavy** ![Vybrat všechny dostupné stavy.](media/04-setup-for-requests.png). Všechny stavy životního cyklu jsou přesunuty do části **Vybrané stavy životního cyklu**.
    - Chcete-li z modelu životního cyklu odstranit stav životního cyklu, vyberte jej v části **Vybrané stavy životního cyklu** a potom vyberte tlačítko šipky vlevo ![Šipka vlevo](media/05-setup-for-requests.png) a přesuňte jej do části Vybrané stavy životního cyklu. pro přesun do části **Zbývající stavy životního cyklu**.

6. Na kartě **Obecné** jsou pole v části **Aktualizace** relevantní, pokud používáte opravu skladu.

    - V poli **Stav životního cyklu u přijatého majetku** vyberte stav životního cyklu majetku, kterým se má automaticky aktualizovat majetek vybraný v požadavku na údržbu, pokud je přijat k opravě.
    - V poli **Stav životního cyklu u doručeného majetku** vyberte stav životního cyklu majetku, kterým se má automaticky aktualizovat majetek vybraný v požadavku na údržbu, jakmile je vrácen po opravě.

Následující ilustrace znázorňuje příklad stránky **Modely životního cyklu požadavků na údržbu**.

![Stránka Modely životního cyklu požadavku na údržbu.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]