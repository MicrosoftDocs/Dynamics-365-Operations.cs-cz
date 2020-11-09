---
title: Povýšení varianty a dokončení experimentu
description: Toto téma popisuje, jak povýšit úspěšnou variantu a dokončit experiment v Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097086"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Povýšení varianty a dokončení experimentu

Toto téma popisuje, jak můžete povýšit variantu, která ve vašem experimentu přinesla nejlepší výsledky, a jak experiment dokončit. Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných tématech.

[ ![Cesta uživatele experimentováním – kontrola a dokončení](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Po [spuštění experimentu](experimentation-run-monitor.md) a shromáždění dostatečných dat, abyste mohli určit, kterou variantu chcete používat na živém webu, můžete danou variantu povýšit a experiment ukončit.

## <a name="promote-a-variation"></a>Povýšení varianty
Pomocí dat a analýz souvisejících s daným experimentem ve službě třetí strany se můžete rozhodnout, která varianta přinesla nejlepší výsledky. Můžete jej pak propagovat nahrazením aktuálního obsahu na živém webu vítěznou variantou, aby byl dostupný všem uživatelům vašeho webu.

Chcete-li propagovat vítěznou variantu, postupujte takto. 

1. V konfigurátoru webů Commerce vyberte **Experimenty** v levém navigačním podokně a poté vyberte experiment.
1. Na panelu nástrojů vyberte **Dokončit experiment**.
1. V nabídce dialogového okna **Dokončení experimentu** vyberte **Zkontrolovat data experimentu**. Otevře se služba třetí strany, ve které můžete ověřit metriku a určit, která varianta fungovala nejlépe.
1. V nabídce dialogového okna **Dokončení experimentu** vyberte vítěznou variantu a pak vyberte **Další**.
1. Otevřete službu třetí strany a experiment zastavte.
1. V konfigurátoru webů vyberte **Dokončit** , pokud chcete přepsat původní živou stránku a publikovat vítěznou variantu tak, aby byla dostupná všem uživatelům vašeho webu. 

> [!NOTE]
> Pokud se rozhodnete zachovat aktuální aktivní živou stránku a žádnou variantu nepublikovat, vyberte **Znovu publikovat původní stránku**.

## <a name="delete-your-experiment"></a>Odstranění experimentu
I když odstranění dokončeného experimentu v Commerce není vyžadováno, můžete ho odstranit, abyste ušetřili místo nebo vyčistili svůj pracovní prostor. 

Chcete-li odstranit experiment v nástroji pro tvorbu obchodních webů, postupujte takto.

1. Vyberte **Experimenty** v levém navigačním podokně a poté vyberte experiment. 
    > [!NOTE]
    > Pokud je experiment stále aktivní, před pokračováním zastavte tento experiment ve službě třetí strany.
1. Na panelu přílazů vyberte **Zrušit publikování** a odeberete obsah varianty ze živého webu.
1. Vyberte **Odstranit** a experiment smažete.

## <a name="previous-step"></a>Předchozí krok
[Spuštění a monitorování experimentu](experimentation-run-monitor.md)
