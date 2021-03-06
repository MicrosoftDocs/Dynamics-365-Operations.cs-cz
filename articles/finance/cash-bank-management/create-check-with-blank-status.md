---
title: Vytvoření šeků se stavem bianko
description: Toto téma vysvětluje, jak vytvořit bianko šeky pro bankovní účet na stránce Šeky.
author: abruer
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1b01daa86055156092d035d61aad78a13349f869
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815949"
---
# <a name="create-checks-that-have-blank-status"></a>Vytvoření šeků se stavem bianko

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit bianko šeky. Můžete například vytvořit bianko šek pro zaznamenání šeku, který byl poškozen a nelze ho použít k platbě.

Na stránce **Šeky** můžete provádět úlohy údržby pro šeky. Můžete například vytvářet nová čísla šeků a odstraňovat šeky. Můžete též vytvářet šeky, které mají stav **Bianko**. Po vytvoření bianko šeků nelze tyto šeky odstranit nebo je v systému použít znovu.

> [!NOTE]
> Tato funkce je k dispozici na stránce **Šeky** pouze tehdy, když zapnete funkci **Vytvoření šeků se stavem bianko na stránce Šeky** na stránce **Správa funkcí**. Pokud není funkce zapnutá, lze šeky se stavem **Bianko** vytvořit pouze z dialogového okna **Platba šekem** během procesu generování platby v závazcích.

Chcete-li otevřít stránku **Šeky**, přejděte na **Pokladna a banka \> Bankovní účty \> Bankovní účty** a potom v podokně akcí na kartě **Řídit platby** ve skupině **Související informace** zvolte **Šeky**. Nebo přejděte na **Pokladna a banka \> Dotazy a sestavy \> Šeky**.

Poté pro vytvoření šeků se stavem **Bianko** zvolte v podokně akcí možnost **Vytvořit bianko šeky**. Když systém vytváří bianko šeky, je přidružený bankovní účet dočasně deaktivován. Toto chování omezuje riziko vygenerování plateb ve stejné době, kdy se vytváří bianko šeky. Po dokončení zpracování bude přidružený bankovní účet znovu aktivován.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]