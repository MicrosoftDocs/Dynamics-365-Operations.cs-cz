---
title: "Stažení konfigurace elektronického vykazování ze služby Lifecycle Services"
description: "Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Stažení konfigurace elektronického vykazování ze služby Lifecycle Services

Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).

Tento kurz vás provede stahováním nejnovější verze konfigurací elektronických sestav (ER) v rámci Microsoft Dynamics Lifecycle Services (LCS).

1.  Přihlaste se k aplikaci Dynamics 365 for Operations použitím některé z následující role:
    -   Návrhář elektronického výkaznictví
    -   Funkční konzultant elektronického výkaznictví
    -   Správce systému

2.  Přejděte do části **Správa organizace** &gt; **Elektronické výkaznictví**.
3.  V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.
4.  Na dlaždici **Microsoft** klepněte na tlačítko **Úložiště**. [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **LCS**. Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:
    1.  Kliknutím na **Přidat** přidejte nové úložiště.
    2.  Vyberte možnost **LCS** jako typ úložiště.
    3.  Klikněte na **Vytvořit úložiště**.
    4.  Zadejte název a popis úložiště.
    5.  Kliknutím na **OK** potvrďte nový záznam úložiště.
    6.  V mřížce vyberte nové úložiště typu **LCS**.

6.  Klepněte na tlačítko **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště. [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Ve stromu konfigurací v levém podokně vyberte konfiguraci ER, kterou potřebujete.
8.  Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.
9.  Kliknutím na tlačítko **Importovat** stáhnete vybranou verzi ze LCS do aktuální instance aplikace Dynamics 365 for Operations. **Poznámka:** Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci aplikace Dynamics 365 for Operations přítomny. [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Poznámka:** V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu. Můžete být upozorněni na potíže se zjištěnou nekonzistencí. Tyto potíže je nutné před importováním verze konfigurace odstranit. Další informace naleznete v seznam souvisejících článků pro toto téma.

<a name="see-also"></a>Viz také
--------

[Přehled elektronického výkaznictví](general-electronic-reporting.md)


