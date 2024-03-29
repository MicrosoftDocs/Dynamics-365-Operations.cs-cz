---
title: Schválení modelu konfigurace produktu
description: Spuštění této procedury vyžaduje, aby nejméně jeden model konfigurace produktu byl k dispozici.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aefc1a26158fd23af7330bfff7a6ac0e8f3e347
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578169"
---
# <a name="approve-a-product-configuration-model"></a>Schválení modelu konfigurace produktu

[!include [banner](../../includes/banner.md)]

Spuštění této procedury vyžaduje, aby nejméně jeden model konfigurace produktu byl k dispozici. Tento postup využívá model špičkového reproduktoru v ukázkové společnosti USMF. Všimněte si, že tento model již byl schválen, ale postup vás provede celým procesem.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pro tuto proceduru vyberte model špičkového reproduktoru.  
1. Vyberte **Verze**.
1. Zvolte **Nové**.
1. V poli **Číslo produktu** zadejte nebo vyberte hodnotu.
    * Odkaz na produkt představuje verzi modelu konfigurace produktu. V seznamu se zobrazí pouze základní produkty, které mají technologii konfigurace založenou na omezeních.  
1. Do pole **Od data** zadejte datum.
    * Vyberte, kdy bude verze modelu produktu k dispozici.  
1. Do pole **Do data** zadejte datum.
    * Vyberte koncové datum, kdy této verzi modelu produktu vyprší platnost, nebo vyberte Nikdy.  
1. Kliknutím na možnost **Schválit** otevřete dialogové okno.
1. V poli **Schválil(a)** zadejte nebo vyberte hodnotu.
    * Vyberte osobu, která je odpovědná za schválení modelů produktu pro použití v operacích.  
1. Vyberte **OK**.
1. Vyberte možnost v poli **Metoda cenových kalkulací**.
    * Aktivujte verzi modelu výrobku. Pro jeden model produktu je možné současně mít aktivní pouze jeden produkt.  
1. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]