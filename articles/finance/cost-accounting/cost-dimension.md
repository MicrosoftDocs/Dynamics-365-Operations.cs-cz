---
title: Vytvoření dimenzí a import členů dimenze
description: Nákladové účetnictví je nezávislý modul vyžadující hlavní data z ostatních modulů.
author: twheeloc
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: twheeloc
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 19c49a3f069274a01741bb272065d17a912970ae
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734044"
---
# <a name="create-dimensions-and-import-dimension-members"></a>Vytvoření dimenzí a import členů dimenze

[!include [banner](../includes/banner.md)]

Nákladové účetnictví je nezávislý modul vyžadující data z ostatních modulů. Tato data lze rozdělit do následujících kategorií:

-  Prvky nákladů
-  Nákladové objekty
-  Statistické dimenze

**Prvek nákladů** odpovídá příslušné položce nákladů v účtové osnově. **Objekt nákladů** odpovídá jakémukoliv typu finanční dimenze, jako například produktům, nákladovým střediskům a projektům, které chcete odhadnout, přímo měřit nebo jim přidělit náklady. **Statistická dimenze** a její členy se používají pro registraci nepeněžních položek. Členy statistické dimenze lze použít jako základ přidělení v distribuci a přidělení nákladů. 

Následující diagram znázorňuje dimenze, které se používají v nákladovém účetnictví.

[![Dimenze nákladového účetnictví.](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

Po importu dat do nákladového účetnictví můžete vytvořit různé perspektivy, které poskytují informace manažerům na všech úrovních organizace. Následující témata obsahují informace o vytváření dimenzí a členech dimenze importu. 

-  [Dimenze prvku nákladů](cost-elements.md)
-  [Vytváření prvků nákladů](./tasks/create-cost-elements.md)
-  [Dimenze objektu nákladů](cost-objects.md)
-  [Mapování členů dimenze prvků nákladů na společnou sadu členů dimenze](map-cost-elements-dimension-members.md)
-  [Namapování dimenze prvku nákladů](./tasks/map-cost-element-dimension.md)
-  [Členy statistické dimenze a šablony poskytovatelů statistických měření](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]
