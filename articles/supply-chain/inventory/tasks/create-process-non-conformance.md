---
title: Vytvoření a zpracování neshody
description: Toto téma vysvětluje provádění správy neshody na základě existující objednávky kvality.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0c0c4415f490219485b3d96fa678a317c1f12f2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204118"
---
# <a name="create-and-process-a-conformance"></a>Vytvoření a zpracování neshody

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje provádění správy neshody na základě existující objednávky kvality. Tento záznam lze spustit v ukázkové společnosti USMF a můžete navrhované hodnoty. Tento postup obvykle provádí úředník řízení kvality.  Nezbytným předpokladem je dokončení pokynů v části [Kontrola kvality zboží](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md). Aby bylo možné zpracovat schválení neshody, uživatel, který spustí záznam úkolu, musí mít hodnotu "Název" přiřazenou na stránce Uživatelé. Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.


## <a name="select-a-quality-order"></a>Vyberte objednávku kvality
1. V podokně navigace přejděte na **Moduly > Řízení zásob > Periodické úlohy > Správa kvality > Objednávky kvality**.
2. V seznamu vyberte objednávku kvality vytvořenou v části [Kontrola kvality zboží](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>Vytvoření neshody
1. V podokně akcí zvolte **Dotazy**.
2. Vyberte **Neshody**.
3. Zvolte **Nové**.
4. V rozevírací nabídce pole **Typ problému** vyberte problém, který byl nalezen během procesu kontroly.  
5. Vyberte **OK**.

## <a name="approvereject-a-nonconformance"></a>Schválení/zamítnutí neshody
1. Vyberte **Funkce**.
2. Vyberte **Schválit neshodu**. V tomto příkladu to je schválení neshody. Schválené neshody lze přidružit k souvisejícím operacím k zaznamenání práce, která je provedena v průběhu zpracování neshody nebo během zpracování oprav jako v tomto tématu.  
3. Vyberte **Ano**.

## <a name="create-a-correction-action"></a>Vytvoření akce opravy
1. Zvolte **Opravy**.
2. Zvolte **Nové**.
3. V poli **Číslo zaměstnance** nového řádku vyberte požadovaný záznam z rozevírací nabídky.
4. Klepněte na tlačítko **Vybrat**.
5. Vyberte **Připojit**. Vytvořte poznámku o opravě. V tomto příkladu akce představuje kontaktování dodavatele za účelem diskuze o případu neshody.  
6. Zvolte **Nové**.
7. Zvolte **Poznámka**. V závislosti na nastavení sestavy lze vytisknout různé typy dokumentů v sestavách, které se vztahují ke správě neshody.  
8. Zadejte hodnotu do pole **Popis**.
9. Zavřete stránku.

## <a name="maintain-a-correction"></a>Údržba opravy
1. Zvolte **Označit jako dokončené**.
2. Vyberte **OK**.
3. Zavřete stránku.

## <a name="close-a-nonconformance"></a>Zavření neshody
1. Vyberte **Funkce**.
2. Vyberte **Zavřít neshodu**.
3. Vyberte **Ano**.
4. Zavřete stránky.
