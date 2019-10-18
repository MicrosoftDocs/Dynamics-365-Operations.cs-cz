---
title: Pracovní příkazy a dlouhodobý majetek
description: Toto téma vysvětluje, jak plánovat pracovní příkazy a dlouhodobý majetek v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250822"
---
# <a name="work-orders-and-fixed-assets"></a>Pracovní příkazy a dlouhodobý majetek


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


V modulu Správa majetku mohou být majetky spojeny v dlouhodobý majetek a pro tyto majetky můžete vytvořit pracovní příkazy. Pokud použijete tuto funkci, můžete získat úplný přehled o dlouhodobém majetku, souvisejících investičních projektech a nákladech registrovaných u investičních projektů v modulu **Řízení projektů a účetnictví** a v modulu **Dlouhodobý majetek**.

>[!NOTE]
>Pole **Číslo dlouhodobého majetku** je vyplněno v projektu úlohy pracovního příkazu pouze v případě, že jako typ projektu v projektu pracovního příkazu je vybrán typ „Investice“.

![Obrázek č. 1](media/24-work-orders.png)

Následující postup popisuje vztah mezi majetkem, pracovními příkazy, projekty úloh pracovních příkazů a dlouhodobým majetkem.

1. Vytvoříte majetek, který spojíte s dlouhodobým majetkem, jak je znázorněno na následujícím obrázku.

![Obrázek č. 2](media/25-work-orders.png)

2. Při nastavení typů pracovních příkazů (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Typy pracovních příkazů**) můžete vytvořit typ pracovního příkazu pro zpracování investic. Viz také [Typy pracovních příkazů](../setup-for-work-orders/work-order-types.md).

![Obrázek č. 3](media/26-work-orders.png)

3. Když nastavíte skupiny projektů pracovních příkazů (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu** >  odkaz **Skupina projektů**), vytvoříte vztah mezi typem pracovního příkazu, který se používá pro investice a skupinu projektů vytvořenou pro investice v modulu **Řízení projektů a účetnictví** (**Řízení projektů a účetnictví** > **Nastavení** > **Účtování** > **Skupiny projektů**).

![Obrázek č. 4](media/27-work-orders.png)

4. Když vytvoříte pracovní příkaz, který se vztahuje k objektu dlouhodobého majetku, vyberte typ pracovního příkazu, který se používá pro zpracování investic, například "investice".

5. Při vytvoření pracovního příkazu se odpovídající typ pracovního příkazu zobrazí ve **Všech pracovních příkazech**.

![Obrázek č. 5](media/28-work-orders.png)

6. Při vytvoření pracovního příkazu je projekt související s pracovním příkazem vytvořen v **Řízení projektů a účetnictví** > **Všechny projekty**. Informace týkající se projektu můžete vidět, kliknete-li na odkaz **ID projektu** na pracovním příkazu (ve **Správě majetku** otevřete pracovní příkaz v zobrazení Podrobnosti > pevná záložka **Podrobnosti řádku** > karta **Obecné** > pole **ID projektu**).

![Obrázek č. 6](media/29-work-orders.png)

7. V modulu **Dlouhodobý majetek** lze zobrazit přehled projektů přiřazených k dlouhodobému majetku (**Dlouhodobý majetek** > **Dlouhodobý majetek** > **Dlouhodobý majetek** > klikněte na položku dlouhodobého majetku v poli **Číslo dlouhodobého majetku** > zobrazení obsahu v podokně **Související informace** > oddíl **Přidružené projekty**).

