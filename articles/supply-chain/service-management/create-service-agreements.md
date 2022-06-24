---
title: Vytváření servisních smluv
description: Tento článek popisuje použití funkcí v modulech Správa servisu a Řízení projektů a účetnictví k vytváření servisních smluv.
author: sorenva
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d18d279cd437e98cad6495def953978cb78e723e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901756"
---
# <a name="create-service-agreements"></a>Vytváření servisních smluv

[!include [banner](../includes/banner.md)]

Tento článek popisuje použití funkcí v modulech Správa servisu a Řízení projektů a účetnictví k vytváření servisních smluv.

## <a name="create-a-service-agreement-from-service-management"></a>Vytvoření servisní smlouvy z modulu Řízení servisu

1. Přejděte na **Správa servisu**.
2. Výběrem možnosti **Servisní smlouvy** vytvoříte nový řádek servisní smlouvy v záhlaví stránky. 
3. Zvolte **Nové**. Zadejte popis, vyberte odkaz na projekt v poli **ID projektu** a vyplňte zbývající pole a řádky servisní smlouvy. Zvolte **Uložit**.
4. Klikněte na kartu **Vztahy** a výběrem možnosti **Předměty servisu** nebo **Servisní úlohy** vytvořte vztahy předmětů servisu nebo vztahy servisních úloh pro servisní smlouvu. Servisní předměty a úlohy, pro které jste vytvořili vztahy, lze přidružit k řádkům na servisní smlouvě.
5. V dolní části stránky vytvořte řádky servisní smlouvy. Tuto akci provedete zkopírováním řádků ze šablony servisu, použitím jiné servisní smlouvy nebo ručním vytvořením řádků servisní smlouvy.

> [!NOTE]
> Pokud do servisní smlouvy zkopírujete řádky z jiné servisní smlouvy, můžete určit, zda chcete také zkopírovat vztahy předmětu servisu a servisní úlohy. Jestliže tyto vztahy zkopírujete, dojde k jejich přidání ke stávajícím vztahům v servisní smlouvě. Pokud zkopírujete řádky servisní smlouvy ze šablony servisu, vztahy servis-objekt a servis-úloha se zkopírují automaticky jako vztahy servis-objekt a servis-úloha v nových řádcích servisní smlouvy.

## <a name="create-service-agreement-lines-manually"></a>Ruční vytvoření řádků servisní smlouvy

1. Ze stránky **Servisní smlouvy** přidejte mřížce řádků řádek servisní smlouvy. 
2. Do řádku servisní smlouvy zadejte příslušné informace. 
3. Výběrem možnosti **Uložit** uložte řádek a poté zavřete stránku.

## <a name="create-a-service-agreement-from-project"></a>Vytvoření servisní smlouvy z projektu

1. Vyberte možnost **Řízení projektů a účetnictví**.
2. Vyberte **Všechny projekty**.
3. Vyberte projekt ze seznamu.
4. V **podokně akcí** vyberte **Spravovat**. Ve skupině **Nová akce** vyberte **Servis** a vyberte **Servisní smlouva**.
5. Postupujte podle kroků v části s názvem **Vytvoření servisní smlouvy** popsané dříve v tomto článku pro zadání odkazu na projekt.


## <a name="related-articles"></a>Související články

[Přehled přípravy a zřízení servisních smluv](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]