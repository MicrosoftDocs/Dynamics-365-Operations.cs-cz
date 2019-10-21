---
title: Vytvoření pracovních příkazů
description: Toto téma vysvětluje, jak vytvořit pracovní příkazy v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a348bc9b7f5a24c5a3ac57113d430a92020b893
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922107"
---
# <a name="creating-work-orders"></a>Vytvoření pracovních příkazů

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Když jste naplánovali preventivní práce údržby můžete v dalším kroku pro práce vytvořit pracovní příkazy. To je možné provést v jednom z rozvrhů údržby. Naplánované práce v rozvrhu údržby mohou mít různé typy odkazů:

| Typ odkazu | Popis                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Plány údržby     | Práce preventivní údržby na základě typů plánu údržby Čas nebo Počítadlo.                       |
| Pořadí údržby    | Práce preventivní údržby obsahující několik majetků, které vyžadují podobný typ údržby.           |
| Požadavek na údržbu   | Ručně vytvořený požadavek na údržbu nebo opravu majetku, který lze převést na pracovní příkaz. |


1. Klikněte na **Správa majetku** > **Společné** > **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvrhu údržby** nebo **Otevřené fondy rozvrhu údržby**.

2. Vyberte naplánované práce údržby, pro které chcete vytvořit pracovní příkaz, a klikněte na **Pracovní příkaz**. V dialogovém okně **Vytvořit pracovní příkazy**, v poli **Hodiny prognózy údržby** se zobrazí celkový počet hodin prognózy pro vybrané řádky.

3. V oddílu **Parametry** vyberte, kolik pracovních příkazů se má vytvořit. Pro každý řádek rozvrhu údržby můžete vytvořit jeden pracovní příkaz, nebo několik pracovních příkazů na základě výběrů v části **Jeden pracovní příkaz na**.

4. Vyberte **Typ pracovního příkazu**, který bude použit pro všechny vytvořené pracovní příkazy. Na následujícím obrázku je uveden příklad dialogového okna **Vytvořit pracovní příkazy**.

![Obrázek č. 1](media/18-preventive-maintenance.png)

5. Klikněte na tlačítko **OK**. Je vytvořen jeden nebo více pracovních příkazů.

