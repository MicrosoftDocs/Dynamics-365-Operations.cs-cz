---
title: Ruční aktualizace čítačů majetku
description: Toto téma popisuje manuální aktualizaci čítačů majetku ve správě majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23a94415a662059ddbd41cc6a0ba9dab24aae44e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889426"
---
# <a name="manual-update-of-asset-counters"></a>Ruční aktualizace čítačů majetku

[!include [banner](../../includes/banner.md)]



Čítače slouží k vytváření registrací majetku, jako jsou například registrace o počtu hodin, kdy byl majetek v provozu, nebo množství, které bylo vyrobeno.

Typ čítače vybraný pro čítač může být nastaven tak, aby zdědil hodnoty čítačů. Jinými slovy, možnost **Zdědit hodnoty čítače majetku** je nastavena na **Ano** na pevné záložce **Obecné** stránky **Čítače** (**Správa majetku** > **Nastavení** > **Typy majetku** > **Čítače**). V takovém případě dojde při vytvoření nového řádku čítače daného typu k automatické aktualizaci všech podřízených položek, které používají stejný typ čítače.

Na stránce **Všechen majetek** vytváříte hodiny nebo registrace čítačů množství na majetku na základě vašich hodnot majetku.

1. Vyberte **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.

2. Vyberte majetek a pak v podokně akcí na kartě **majetek** ve skupině **Preventivní** vyberte možnost **čítače**. Na stránce **Čítače majetku** se zobrazí seznam všech předchozích registrací čítačů u vybraného majetku.

3. Zvolte **Nový** pro vytvoření registrace. ID majetku je automaticky zadáno do pole **Majetek**.

4. V poli **Čítač** vyberte relevantní čítač. Vybrat lze pouze čítače související s typem majetku vybraným pro majetek. Související jednotka je automaticky zadána do pole **Jednotka**.

5. V poli **zaregistrováno** vyberte datum a čas pro registraci čítače.

6. Do pole **Hodnota** zadejte číslo od poslední registrace čítače. Případně zadejte do pole **Agregovaná hodnota** číslo celkového součtu.

Mějte na paměti následující body:

- Pokud fyzicky instalujete do majetku nový čítač, je nutné provést registraci v položce majetku na stránce **Čítače majetku**. Dále je nutné vytvořit dva řádky pro registraci, které mají totožná časová razítka. První řádek musí být pro čítač, který nahrazujete. V řádku, který se vztahuje k novému čítači, zaškrtněte políčko **Vynulovat čítač**. V poli **Celkem** je celkové číslo součtem čítače všech registrovaných hodnot tohoto typu čítače.

- Pokud je u majetku zaškrtnuto políčko **Vynulovat čítač** s použitím plánu údržby s typem intervalu "jednou z..." nebo "po dosažení...", čítač je v novém řádku čítače stále aktivní, protože vytváříte oddělený řádek čítače a začínáte znovu s novým čítačem.

Následující ilustrace znázorňuje příklad stránky **Čítače majetku**.

![Obrázek č. 1](media/11-work-orders.png)

Na stránce **Čítače majetku** (**Správa majetku** > **Dotazy** > **Majetek** > **Čítače majetku**) můžete zaregistrovat čítače u několika majetků najednou.

>[!NOTE]
>Rozsah lze nastavit tak, aby definoval odchylky v ručních registracích čítačů. Můžete také určit typ zprávy, která se zobrazí v případě, že se registrace nacházejí mimo definovaný rozsah. Další informace o nastavení čítačů naleznete v tématu [Čítače](../setup-for-objects/counters.md).

