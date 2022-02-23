---
title: Rozdělení generovaných souborů XML na základě velikosti souboru a množství obsahu
description: Toto téma obsahuje informace o rozdělení generovaných souborů na základě velikost souboru a množství položek obsahu.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: d60266aba42f502e7707bdace921cfee4526b6ae
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682864"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Rozdělení generovaných souborů XML na základě velikosti souboru a množství obsahu

[!include[banner](../includes/banner.md)]

Formáty elektronického výkaznictví (ER) můžete navrhovat pro generování odchozích dokumentů ve formátu XML. V některých případech je možné tyto dokumenty přijmout, pouze pokud splňují konkrétní kritéria, jako je maximální velikost souboru nebo maximální počet některých uzlů XML. Můžete navrhovat formáty ER ke generování elektronických dokumentů, které splňují požadavky, které určují příjemci těchto dokumentů.

- Pro prvek formátu SOUBORU můžete definovat limit velikosti souboru jako výraz ER. Pokud je při generování vyúčtování ER překročen definovaný limit, ER dokončí vytvoření aktuálního souboru a pak se přesune k vytvoření dalšího souboru.
- Pro libovolný formát prvku XML můžete definovat limit počtu prvků jako výraz ER. Pokud počet uzlů XML v generovaném souboru překročí definovaný limit, když je spuštěná sestava ER, ER dokončí vytvoření aktuálního souboru a pak se přesune k vytvoření dalšího souboru.
- Pro libovolný prvek formátu XML SEQUENCE můžete definovat limit počtu podržízených prvků jako výraz ER. Pokud počet vnořených uzlů XML prvku formátu v generovaném souboru překročí definovaný limit, když je spuštěná sestava ER, ER dokončí vytvoření aktuálního souboru a pak se přesune k vytvoření dalšího souboru.
- Libovolný prvek formátu XML ELEMENT můžete označit jako nerozdělitelný. Tímto způsobem můžete udržovat vnořené položky XML uzlů, které jsou generovány v rámci formátu prvku v jednom generované souboru.

Kromě použití prvků formátu XML ELEMENT a XML SEQUENCE pro přidání uzlů XML do generovaného souboru můžete použít prvek formátu RAW XML. Uzly, které přidáte pomocí prvku formátu RAW XML nejsou však brány v úvahu, když je vypočten počet uzlů pro posouzení limitu počtu prvků.

Pokud jste nakonfigurovali cíle souboru pro prvek formátu FILE, který byl konfigurován pro rozdělení generovaného výstupu při každém překročení určitého limitu, každá část generovaného výstupu je zaslána do konfigurovaného cíle souboru jako samostatný soubor. Aby bylo možné jedinečně pojmenovat soubory, které jsou vytvořeny rozdělením výstupu, musíte nakonfigurovat výraz ER pro prvek formátu FILE. Pokud zahrnete zdroj dat ER typu NUMBER SEQUENCE, číselná řada se zvýší pro každou část rozděleného výstupu.

Další informace o této funkci zobrazíte přehráním Průvodce záznamem úloh **ER rozdělení souborů xml na základě velikosti souboru nebo množství položek obsahu**, která je součástí obchodního procesu **7.5.4.3 Acquire/Develop IT service/solution components (10677)** a dá se stáhnout ze [služby Stažení softwaru Microsoft](https://go.microsoft.com/fwlink/?linkid=874684). Tento průvodce záznamem úloh vás provede procesem konfigurace formátu ER pro rozdělení generovaných souborů na základě limitů velikosti souboru a množství položek obsahu. Pro dokončení průvodce záznamem úloh si musíte stáhnout následující soubory:

- [Konfigurace modelu ER - XmlFilesSplittingModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [Konfigurace formátu ER – XmlFilesSplittingFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a>Další zdroje
[Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)
