---
title: "Vykazování daně z prodeje pro Českou republiku | Dokumentace Microsoftu"
description: "Toto téma uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku."
author: LizaGolub
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: TaxGroup, VendParameters
audience: Application User
ms.reviewer: shylaw
ms.suite: Released- Dynamics AX application 7.0.1
ms.custom: 1696023
ms.assetid: 219d7cd6-c517-403e-92c5-6a70bfb39354
ms.search.region: Czech Republic
ms.author: v-elgolu
ms.translationtype: Human Translation
ms.sourcegitcommit: fd42fe23b30fe163a003614d6cbe9ff24ae38c5d
ms.openlocfilehash: bfa6c79c1bd45e63c5b333c1fa1d908a59ec3b1a
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="sales-tax-reporting-for-the-czech-republic"></a>Vykazování daně z prodeje pro Českou republiku

Toto téma uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku. 

Když právnické osoby, které mají svou primární adresu v České republice, nakupují od členských států Evropské unie (EU), měly by provést vlastní vyměření daně z přidané hodnoty (DPH), aby se zajistilo, že jsou splněny následující podmínky:

-   DPH na výstupu se platí v období DPH, kdy byla vystavena faktura (datum dokumentu).
-   DPH na vstupu nebyla odečtena před přijetím dokumentu (datum rejstříku DPH).

Informace o intrakomunitární DPH mohou být vypočteny a zaúčtovány automaticky. Při zaúčtování faktury dodavatele v Evropské unii (EU) jsou vytvořeny dvě transakce DPH ve stejné výši. Jedna transakce DPH je vytvořena pro závazek prodejní daně a druhá pro pohledávku prodejní daně. Aby se tento požadavek projevil v aplikaci Microsoft Dynamics 365 for Operations, je třeba nastavit následující hodnoty:

-   Zaškrtněte políčko **DPH intrakomunitárního plnění** na stránce **Parametry závazků** (**Závazky** &gt; **Nastavení** &gt; **Parametry závazků**).
-   Zaškrtněte políčko **Datum dokumentu pro intrakomunitární DPH** na stránce **Parametry závazků**.
-   Vytvořte dva kódy daně z prodeje: jeden, který má kladné procento daně z prodeje a druhý, který má záporné procento daně z prodeje.
-   Vytvořte skupinu daně z prodeje obsahující kladné i záporné kódy daně z prodeje. Pro záporný kód daně z prodeje vyberte parametr **DPH intrakomunitárního plnění**.
-   V denících vyberte parametr **Datum dokumentu pro intrakomunitární DPH**.

Při zaúčtování nákupní faktury, pohledávka DPH a závazek DPH jsou účtovány ve stejnou dobu. V případě kladných transakcí daně z prodeje je datum registru DPH nastaveno na datum registru DPH ze stránky zaúčtování faktury a směrování daně z prodeje je **DPH na vstupu**. V případě záporných transakcí daně z prodeje je datum registru DPH nastaveno na datum dokumentu a směrování daně z prodeje je **DPH na výstupu**.


