---
title: Delegování pracovních položek ve workflowu
description: Pokud plánujete být mimo kancelář nebo nemůžete reagovat na pracovní položku, můžete předat nebo znovu přiřadit své pracovní položky jinému uživateli.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72ffe8123203123b75ea424814393d73ea8f728078e9e34fe903e5944ec11cfb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749549"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegování položek práce ve workflow

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Ručně delegování pracovní položky

Pokud chcete delegovat oprávnění pro jednotlivé pracovní položky, vyberte možnost **Delegovat** v nabídce **Workflow** a zadejte uživatele k delegování a komentář. Tím bude pracovní položka znovu přiřazena danému uživateli, aby ji mohl dokončit.

## <a name="manually-delegate-multiple-work-items"></a>Ruční delegování více pracovních položek

Více pracovních položek lze delegovat najednou na stránce **Pracovní položky přiřazené mně**. Pro hromadné delegování jsou způsobilé následující typy pracovních postupů: pracovní postup schvalování kupní smlouvy, pracovní postup nákupní objednávky, kontrola nákupní žádanky a pracovní postup faktury dodavatele. Funkce **delegování více pracovních položek** je ve výchozím nastavení zakázána a lze ji povolit v nabídce **Pracovní prostory > Správa funkcí**. Chcete-li pomoci s povolením této funkce, obraťte se na správce systému.
1.  Přejděte na **Společné > Společné > Pracovní položky > Pracovní položky přiřazené mně**.
2.  Vyberte pracovní položky, které mají být delegovány.
3.  Klikněte na nabídku **Delegování pracovních položek**.
4.  V poli **Uživatel** vyberte uživatele, kterému chcete pracovní položku delegovat.
5.  Do pole **Komentář** zadejte komentář s vysvětlením, proč delegujete pracovní položky.
6.  Klikněte na tlačítko **Delegovat pracovní položky**. Tím se delegování pracovní položky provede.

## <a name="automatically-delegate-work-items"></a>Automatické delegování pracovních položek

Pokud plánujete absenci v kanceláři nebo nejste jinak schopní u pracovních položek nějakou dobu jednat, můžete automaticky delegovat nové pracovní položky na ostatní uživatele pomocí stránky **Uživatelské možnosti**.

### <a name="set-up-automatic-delegation"></a>Nastavení automatického předávání
1. Přejděte na **Společné > Nastavení > Možnosti uživatelů**.
2. Klikněte na kartu **Workflow**. Zkontrolujte, zda je rozbalen oddíl Delegování. Chcete-li nakonfigurovat systém tak, aby automaticky delegoval vaše pracovní položky ostatním uživatelům, je nutné vytvořit pravidla delegování, která určí, kdy se budou delegovat určité typy pracovních položek. Při vytváření pravidla delegování postupujte takto:  
3. Klikněte na tlačítko **Přidat**.
4. Vyberte volbu v poli **Rozsah**:
    - Vše - Delegování všech pracovních položek, které máte přiřazeny.
    - Modul – Delegování pouze pracovních položek, které máte přiřazeny pro specifický typ workflowu. Pokud vyberete tuto možnost, je nutné vybrat typ workflowu v poli **Název**.
    - Workflow – Delegování pouze pracovních položek, které máte přiřazeny pro specifický workflow. Pokud vyberete tuto možnost, je nutné vybrat workflow v poli **Název**.  
5. V poli **Název**:
    - Pro rozsah **Modul** vyberte cílový modul.
    - Pro rozsah **Workflow** vyberte cílový workflow.
6. V poli **Delegovat** vyberte uživatele, kterému chcete pracovní položku delegovat. Použijte pole **Počáteční datum a čas** a **Koncové datum a čas** k určení, kdy mají být pracovní položky automaticky delegovány.  
7. Do pole **Počáteční datum a čas** zadejte datum a čas.
8. Do pole **Koncové datum a čas** zadejte datum a čas.
9. Zaškrtnutím políčka **Povoleno** můžete aktivovat pravidlo delegování. 
10. Do pole **Komentář** zadejte komentář s vysvětlením, proč delegujete pracovní položky.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]