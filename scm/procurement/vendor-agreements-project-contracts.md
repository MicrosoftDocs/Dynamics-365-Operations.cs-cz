---
title: "Smlouvy s dodavatelem s platbou po zaplacení"
description: "Tento článek vysvětluje podmínky PWP (platby po zaplacení) pro smlouvy s dodavatelem. Podmínky PWP umožňují částečně nebo plně zadržet platbu dodavateli, dokud vám nezaplatí odběratel v projektu. Tento článek také obsahuje příklad ze života, který popisuje, jak používat podmínky PWP u projektu."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjProjectsListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23131
ms.assetid: 20bf1d7f-8813-4c69-9cd7-576884a7e169
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 0ca75dbd00ad260c911a323f17717d0ff83331dd
ms.lasthandoff: 03/31/2017


---

# <a name="pay-when-paid-vendor-agreements"></a>Smlouvy s dodavatelem s platbou po zaplacení

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje podmínky PWP (platby po zaplacení) pro smlouvy s dodavatelem. Podmínky PWP umožňují částečně nebo plně zadržet platbu dodavateli, dokud vám nezaplatí odběratel v projektu. Tento článek také obsahuje příklad ze života, který popisuje, jak používat podmínky PWP u projektu.

Po schválení dodavatele jako subdodavatele pro projekt lze zadržet platby dodavateli nebo subdodavateli, dokud nebudete odběratelem zaplaceni za projekt. Chcete-li zadržet platbu dodavateli, nastavte podmínky platby po zaplacení (PWP) při nastavení nákupní objednávky u dodavatele. Při vytvoření nákupní objednávky pro dodavatele a přiřazení ID projektu k nákupní objednávce, podmínky PWP v projektu jsou přidruženy k nákupní objednávce a dodavateli. Na stránce **Faktury dodavatele s platbou po zaplacení** můžete zobrazit seznam nezaplacených faktur dodavatele pro nákupní objednávku a faktury přidružené k odběrateli. Tento formulář slouží k určení, zda a jak je třeba dodavateli zaplatit. Například když odběratel zaplatí částku uvedenou na faktuře projektu, můžete uvolnit část nebo všechny související faktury dodavatele pro platbu. Můžete nastavit podmínky PWP a určit, že dodavatel bude vyplacen poté, co obdržíte určitou poměrnou část související platby od odběratele. Když obdržíte částečnou platbu obdržíte od odběratele, můžete některé související faktury dodavatele k platbě vydat ručně. Následující příklad ukazuje, jak můžete využít podmínky PWP k zadržení platby pro dodavatele nebo subdodavatele, dokud vám odběratel nezaplatí. Vaše organizace uzavře s odběratelem smlouvu o poskytnutí 100 počítačů, do kterých nainstalujete softwaru, který odběratel požaduje. Cena, na které se s odběratelem dohodnete, je 150,00 za každý počítač. K dodání počítačů využijete služby dodavatele třetí strany. Odběratel chce schválit kvalitu počítačů, než vaší organizaci zaplatí. Zásadou vaší organizace je zadržení platby jinému dodavateli, dokud vám odběratel za projekt nezaplatí. Proto nastavíte projekt s procentem PWP na 100 procent, aby bylo možné pozdržet všechny platby dodavateli, dokud neobdržíte celou platbu za fakturu odběratele. Dodavatel si za každý počítač účtuje 100,00. Dodavatel vám odešle počítače. Dodávka zahrnuje fakturu v hodnotě 10 000,00 za 100 počítačů. Vzhledem k tomu, že jste nastavili projekt s podmínkami PWP, neplaťte dodavateli. Jakmile od dodavatele obdržíte počítače, nainstalujte požadovaný software do počítačů. Jakmile odešlete počítače odběrateli, odešlete také odběrateli fakturu v hodnotě 15 000,00. Odběratel počítače zkontroluje a schválí kvalitu výrobku. Odběratel pak zaplatí organizaci celou částku faktury projektu. Poté, co obdržíte celou platbu od odběratele, můžete zaplatit dodavateli celou částku faktury dodavatele, 10 000,00.




