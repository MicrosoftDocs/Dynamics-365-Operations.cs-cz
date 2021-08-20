---
title: Pracovní příkazy a dlouhodobý majetek
description: Toto téma vysvětluje, jak plánovat pracovní příkazy a dlouhodobý majetek v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad4af6bb0df557314f844d3e7a6c5fb84a6331d86f16e1bc76150f78ce3039e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752795"
---
# <a name="work-orders-and-fixed-assets"></a>Pracovní příkazy a dlouhodobý majetek

[!include [banner](../../includes/banner.md)]


V modulu Správa majetku mohou být majetky spojeny v dlouhodobý majetek a pro tyto majetky můžete vytvořit pracovní příkazy. Pokud použijete tuto funkci, můžete získat úplný přehled o dlouhodobém majetku, souvisejících investičních projektech a nákladech registrovaných u investičních projektů v modulu **Řízení projektů a účetnictví** a v modulu **Dlouhodobý majetek** v Microsoft Dynamics 365 for Finance and Operations.

>[!NOTE]
>Pole **Číslo dlouhodobého majetku** je vyplněno v projektu úlohy pracovního příkazu pouze v případě, že jako typ projektu v projektu pracovního příkazu je vybrán typ **Investice**.

Na následujícím obrázku je znázorněn vztah mezi investičním projektem v modulu **řízení projektu a účetnictví** a projektem pracovního příkazu.

![Obrázek č. 1.](media/24-work-orders.png)

Následující postup popisuje vztah mezi majetkem, pracovními příkazy, projekty úloh pracovních příkazů a dlouhodobým majetkem.

1. Vytvoříte majetek, který je spojen s dlouhodobým majetkem.

![Obrázek č. 2.](media/25-work-orders.png)

2. Při nastavení typů pracovních příkazů na stránce **Typy pracovních příkazů** (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Typy pracovních příkazů**) můžete vytvořit typ pracovního příkazu pro zpracování investic. Viz také [Typy pracovních příkazů](../setup-for-work-orders/work-order-types.md).

![Obrázek č. 3.](media/26-work-orders.png)

3. Když nastavíte skupiny projektů pracovních příkazů na kartě **Skupina projektů** stránky **Nastavení projektu pracovního příkazu** (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu**), vytvoříte vztah mezi typem pracovního příkazu, který se používá pro investice a skupinu projektů vytvořenou pro investice na stránce **Skupiny projektu** v modulu **Řízení projektů a účetnictví** (**Řízení projektů a účetnictví** > **Nastavení** > **Účtování** > **Skupiny projektů**).

![Obrázek č. 4.](media/27-work-orders.png)

4. Když vytvoříte pracovní příkaz, který se vztahuje k objektu dlouhodobého majetku, vyberte typ pracovního příkazu, který se používá pro zpracování investic, například **Investice**.

5. Při vytvoření pracovního příkazu se odpovídající typ pracovního příkazu zobrazí na stránce **Všechny pracovní příkazy**.

![Obrázek č. 5.](media/28-work-orders.png)

6. Po vytvoření pracovního příkazu se na stránce **Všechny projekty** v modulu **Řízení projektů a účetnictví** vytvoří projekt související s pracovním příkazem (**Řízení projektů a účetnictví** > **Projekty** > **Všechny projekty**). Chcete-li zobrazit informace související s projektem, vyberte odkaz v poli **ID projektu** na kartě **Obecné** na pevné záložce **Podrobnosti řádku** v zobrazení Podrobnosti na stránce **Všechny pracovní příkazy** v modulu **Správa majetku** (**Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy**).

![Obrázek č. 6.](media/29-work-orders.png)

7. Chcete-li zobrazit přehled projektů spojených s dlouhodobým majetkem, vyberte možnost **Dlouhodobý majetek** > **Dlouhodobý majetek** > **Dlouhodobý majetek** a pak v poli **Číslo dlouhodobého majetku** otevřete zobrazení podrobností. Rozbalte podokno **Související informace** na pravé straně stránky a vyberte pevnou záložku **Související projekty**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]