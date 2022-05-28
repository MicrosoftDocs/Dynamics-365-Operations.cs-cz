---
title: 'Vytváření objektů nákladů  '
description: Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska v nákladovém účetnictví prostřednictvím datového konektoru.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734123"
---
# <a name="create-cost-objects"></a>Vytváření objektů nákladů   

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska v nákladovém účetnictví prostřednictvím datového konektoru. K vytvoření této procedury byla použita ukázková společnost USMF. 


## <a name="create-new-cost-objects"></a>Vytvoření nových objektů nákladů
1. Přejděte na položky **Nákladové účetnictví > Dimenze > Dimenze objektu nákladů**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Název**.
4. V poli **Datový konektor pro členy dimenzí** zadejte nebo vyberte hodnotu.
5. Zadejte hodnotu do pole **Popis**.
6. Klikněte na tlačítko **Uložit**.

## <a name="configure-the-data-connector"></a>Konfigurace datového konektoru
1. Klikněte na **Konfigurovat poskytovatele členů dimenzí**.
    * Vyberte CostCenter pro import dimenze CostCenter do nákladového účetnictví.  
2. V poli **Název dimenze** vyberte Nákladové středisko.
3. Klikněte na tlačítko **OK**.

## <a name="import-cost-centers"></a>Import nákladových středisek
1. Klikněte na **Importovat členy dimenze**.
2. Klikněte na tlačítko **OK**.

## <a name="view-the-imported-cost-centers"></a>Zobrazení importovaných nákladových středisek
1. Klikněte na **Zobrazit členy dimenze**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
