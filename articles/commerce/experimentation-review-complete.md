---
title: Povýšení varianty a dokončení experimentu
description: Toto téma popisuje, jak povýšit úspěšnou variantu a dokončit experiment v Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930152"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Povýšení varianty a dokončení experimentu

Toto téma popisuje, jak můžete povýšit variantu, která ve vašem experimentu přinesla nejlepší výsledky, a jak experiment dokončit. Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných tématech.

[ ![Cesta uživatele experimentováním – kontrola a dokončení](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Po [spuštění experimentu](experimentation-run-monitor.md) a shromáždění dostatečných dat, abyste mohli určit, kterou variantu chcete používat na živém webu, můžete danou variantu povýšit a experiment ukončit.

## <a name="promote-a-variation"></a>Povýšení varianty
Pomocí dat a analýz souvisejících s daným experimentem ve službě třetí strany se můžete rozhodnout, která varianta přinesla nejlepší výsledky. Když budete chtít nahradit aktuální obsah na živém webu vítěznou variantou, aby byl dostupný všem uživatelům vašeho webu, postupujte následovně. 

1. Přejděte na kartu **Experimenty** v konfigurátoru webů a vyberte příslušný experiment.
1. Na horním panelu vyberte **Dokončit experiment** .
1. V nabídce dialogového okna **Dokončení experimentu** vyberte **Zkontrolovat data experimentu** . Otevře se služba třetí strany, ve které můžete ověřit metriku a určit, která varianta fungovala nejlépe.
1. V nabídce dialogového okna **Dokončení experimentu** v konfigurátoru webů vyberte vítěznou variantu a pak vyberte **Další** .
1. Otevřete službu třetí strany a experiment zastavte.
1. V konfigurátoru webů vyberte **Dokončit** , pokud chcete přepsat původní živou stránku a publikovat vítěznou variantu tak, aby byla dostupná všem uživatelům vašeho webu. 

> [!NOTE]
> Pokud se rozhodnete zachovat aktuální aktivní živou stránku a žádnou variantu nepublikovat, vyberte **Znovu publikovat původní stránku** .

## <a name="delete-your-experiment"></a>Odstranění experimentu
I když odstranění dokončeného experimentu v Commerce není vyžadováno, můžete ho odstranit, abyste ušetřili místo nebo vyčistili svůj pracovní prostor. Experiment můžete odstranit následujícím postupem.

1. Přejděte na kartu **Experimenty** v konfigurátoru webů a vyberte příslušný experiment. 
    > [!NOTE]
    > Pokud je experiment stále aktivní, před pokračováním zastavte tento experiment ve službě třetí strany.
1. Výběrem možnosti **Zrušit publikování** na panelu příkazů odeberete obsah varianty ze živého webu.
1. Výběrem možnosti **Odstranit** na panelu příkazů experiment odstraníte.

## <a name="previous-step"></a>Předchozí krok
[Spuštění a monitorování experimentu](experimentation-run-monitor.md)
