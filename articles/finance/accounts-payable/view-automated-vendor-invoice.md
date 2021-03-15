---
title: Zobrazení výsledků automatizace faktur dodavatelů (náhled)
description: Toto téma vysvětluje, jak zobrazit stav dodavatelských faktur, které jsou v automatizovaném procesu odesílání do pracovního postupu.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: baa2f1f55dfb9bb93b4f27c45db563e39850dd37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969719"
---
# <a name="view-vendor-invoice-automation-results"></a>Zobrazení výsledků automatizace faktur dodavatele

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak zobrazit stav dodavatelských faktur, které jsou v automatizovaném procesu odesílání do pracovního postupu. Podrobnosti o historii automatizace se uchovávají pro každou importovanou fakturu dodavatele. V závislosti na obchodních procesech, které jste u vás automatizovali, zobrazuje stránka **Čekající faktury dodavatele** hodnoty **Stav shody automatického potvrzení** a **Stav automatizovaného odeslání do pracovního postupu**. Můžete si zobrazit podrobnosti a vytvořit plán zaměřující se na faktury, u nichž automatický krok selhal. Až pak problém opravíte, můžete pokračovat v automatizovaném procesu pro importovanou fakturu.

Před úpravou odeslané faktury musíte pozastavit automatické zpracování. Pokud musí být faktura v automatizovaném procesu odesílání do pracovního postupu pozastavena, nastavte pole **Zahrnout do automatizovaného zpracování** na **Ne** na stránce **Faktury dodavatele**. Automatizace pak nepoběží, dokud **Zahrnout do automatizovaného zpracování** nenastavíte na **Ano**. U faktury lze pozastavit další automatizaci, pokud ještě není v systému pracovního postupu a není používána automatizovaným procesem.

Pokud importovaná faktura podléhá procesu odeslání do pracovního postupu, můžete si zobrazit její hodnotu **Stav automatizace** na stránce **Faktury dodavatele**. Sledují se následující stavy:

- **Zahrnuto** – Automatizované procesy definované na stránce **Parametry závazků** běží správně, ale ještě nebyly dokončeny.
- **Pozastaveno** – Automatizované procesy definované na stránce **Parametry závazků** proběhly, ale nejméně jeden krok procesu selhal. Stav **Pozastaveno** se použije také v případě, že je pole **Zahrnout do automatizovaného zpracování** nastaveno na **Ne**. Selhání si můžete prohlédnout výběrem volby **Zobrazit poslední výsledky**.
- **V pracovním postupu** – Importovaná faktura byla odeslána do systému pracovního postupu, a to buď automatizovaným procesem odeslání do pracovního postupu, nebo ručně.
- **Pracovní postup dokončen** – Proces u importované faktury byl dokončen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]