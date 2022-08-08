---
title: Vytvoření šeků se stavem bianko
description: Tento článek vysvětluje, jak vytvořit bianko šeky pro bankovní účet.
author: angelad116
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8d3f3857fe5261c1c95d02f3b7c7aaf9db7c096f
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151573"
---
# <a name="create-checks-that-have-blank-status"></a>Vytvoření šeků se stavem bianko

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak vytvořit bianko šeky. Můžete například vytvořit bianko šek pro zaznamenání šeku, který byl poškozen a nelze ho použít k platbě.

Na stránce **Šeky** můžete provádět úlohy údržby pro šeky. Můžete například vytvářet nová čísla šeků a odstraňovat šeky. Můžete též vytvářet šeky, které mají stav **Bianko**. Po vytvoření bianko šeků nelze tyto šeky odstranit nebo je v systému použít znovu.

> [!NOTE]
> Tato funkce je k dispozici na stránce **Šeky** pouze tehdy, když zapnete funkci **Vytvoření šeků se stavem bianko na stránce Šeky** na stránce **Správa funkcí**. Pokud není funkce zapnutá, lze šeky se stavem **Bianko** vytvořit pouze z dialogového okna **Platba šekem** během procesu generování platby v závazcích.

Chcete-li otevřít stránku **Šeky**, přejděte na **Pokladna a banka \> Bankovní účty \> Bankovní účty** a potom v podokně akcí na kartě **Řídit platby** ve skupině **Související informace** zvolte **Šeky**. Nebo přejděte na **Pokladna a banka \> Dotazy a sestavy \> Šeky**.

Poté pro vytvoření šeků se stavem **Bianko** zvolte v podokně akcí možnost **Vytvořit bianko šeky**. Když systém vytváří bianko šeky, je přidružený bankovní účet dočasně deaktivován. Toto chování omezuje riziko vygenerování plateb ve stejné době, kdy se vytváří bianko šeky. Po dokončení zpracování bude přidružený bankovní účet znovu aktivován.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
