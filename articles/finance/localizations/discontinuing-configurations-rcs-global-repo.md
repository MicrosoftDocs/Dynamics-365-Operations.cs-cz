---
title: Ukončení konfigurací v globálním úložišti RCS
description: Toto téma popisuje, jak ukončit konfigurace v globálním úložišti RCS.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018726"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Ukončení konfigurací v globálním úložišti RCS

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak ukončit konfiguraci v globálním úložišti RCS. Dříve bylo možné odstranit pouze konfigurace, které již nebyly potřebné. Nyní však můžete označit uvolněnou konfiguraci jako **Zrušenou** v globálním úložišti RCS. Touto funkcí můžete provést také následující: 
 
 - Poskytnout předem oznámení, když se plánuje ukončení konfigurace.
 - Uvést příslušné podrobnosti o náhradní konfiguraci.
 - Nastavit datum **Podporováno do** pro konkrétní konfiguraci s cílem informovat uživatele, kdy bude ukončena.

Když ukončíte verzi konfigurace, můžete zadat následující volitelné informace:

  - **Náhradní konfigurace**
  - **Verze náhradní konfigurace**
  - **Volná textová poznámka**: Toto pole použijte k poskytnutí odkazů na dokumentaci nebo odkazů
  - **Podporováno do**: Toto pole poskytuje navrhované datum, do kterého bude podporována aktuální konfigurace/verze. Toto datum musí být aktualizováno ručně.
  
Chcete-li konfiguraci ukončit, proveďte následující kroky. 

1. Vyberte, zda chcete ukončit jednu verzi, nebo všechny verze se stejným nastavením v jedné operaci nastavením **Všechny verze** na **Ano**. 
2. Nastavte parametr **Ukončit** na **Ano**.
3. Vyberte **OK** k ukončení konfigurací. Pole **Datum ukončení** pole se vyplní, když uložíte změny.

![Informace o ukončení konfigurace](media/Discontinue-details-2.png)
  
Konfiguraci můžete vrátit zpět na **Sdílená** nebo kdykoli upravit informace o ukončení. Pokud sdílíte konfiguraci, zadejte datum **Podporováno do** a všechny další informace související s ukončením, aby byly uvedeny vaše plány pro budoucí ukončení.

Pokud chcete sdílet informace o plánovaném ukončení, může uživatel před vyplněním všech polí předvyplnit všechna pole související s výměnou, ale ponechat parametr **Ukončit** nastavený na **Ne**.

> [!NOTE]
> Ukončení neomezuje operace s konfiguracemi. Konfigurace můžete nadále importovat, spouštět nebo odvozovat, tato pole jsou informační.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finance podporuje zobrazování těchto informací od verze 10.0.14

Od verze 10.0.14 Dynamics 365 Finance podporuje zobrazování informací o přerušení. Na stránce **Globální úložiště** můžete zobrazit aktuální informace týkající se ukončení. Ve výchozím nastavení jsou odfiltrovány konfigurace, které jsou přerušeny.
  
Stránka **Importované konfigurace** (ERSolutionTable) zobrazuje konfigurace, které již byly při importu ukončeny. U těch konfigurací, které byly po importu ukončeny, lze informace o ukončení synchronizovat spuštěním úlohy **Importovat aktualizace konfigurací**.


