---
title: Vytvoření dimenzí a import členů dimenze
description: Nákladové účetnictví je nezávislý modul vyžadující hlavní data z ostatních modulů.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3eedce9cd092f9c299a2381a28a801351f15c4cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226382"
---
# <a name="create-dimensions-and-import-dimension-members"></a>Vytvoření dimenzí a import členů dimenze

[!include [banner](../includes/banner.md)]

Nákladové účetnictví je nezávislý modul vyžadující data z ostatních modulů. Tato data lze rozdělit do následujících kategorií:

-  Prvky nákladů
-  Nákladové objekty
-  Statistické dimenze

**Prvek nákladů** odpovídá příslušné položce nákladů v účtové osnově. **Objekt nákladů** odpovídá jakémukoliv typu finanční dimenze, jako například produktům, nákladovým střediskům a projektům, které chcete odhadnout, přímo měřit nebo jim přidělit náklady. **Statistická dimenze** a její členy se používají pro registraci nepeněžních položek. Členy statistické dimenze lze použít jako základ přidělení v distribuci a přidělení nákladů. 

Následující diagram znázorňuje dimenze, které se používají v nákladovém účetnictví.

[![Dimenze nákladového účetnictví](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

Po importu dat do nákladového účetnictví můžete vytvořit různé perspektivy, které poskytují informace manažerům na všech úrovních organizace. Následující témata obsahují informace o vytváření dimenzí a členech dimenze importu. 

-  [Dimenze prvku nákladů](cost-elements.md)
-  [Vytváření prvků nákladů](./tasks/create-cost-elements.md)
-  [Dimenze objektu nákladů](cost-objects.md)
-  [Mapování členů dimenze prvků nákladů na společnou sadu členů dimenze](map-cost-elements-dimension-members.md)
-  [Namapování dimenze prvku nákladů](./tasks/map-cost-element-dimension.md)
-  [Členy statistické dimenze a šablony poskytovatelů statistických měření](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]