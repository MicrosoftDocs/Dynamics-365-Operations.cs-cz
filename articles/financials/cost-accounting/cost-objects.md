---
title: "Dimenze objektu nákladů"
description: "Když analyzujete náklady, používáte ke stanovení, kam jsou náklady převáděny, dimenze prvku nákladů. Dimenze objektu nákladů používáte k určení, kde byste měli přiřadit náklady. V tomto tématu jsou informace o dimenzích objektu nákladů."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8195b776e5d46485172c9f5550ab4ed6d8623dfc
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="cost-object-dimensions"></a>Dimenze objektu nákladů

[!include[banner](../includes/banner.md)]


Když analyzujete náklady, používáte ke stanovení, kam jsou náklady převáděny, dimenze prvku nákladů. Dimenze objektu nákladů používáte k určení, kde byste měli přiřadit náklady. V tomto tématu jsou informace o dimenzích objektu nákladů.

Objekt nákladů může být jakýkoliv typ objektu, který chcete odhadnout, přidělit k němu náklady nebo přímo změřit. Typické objekty nákladů zahrnují produkty, projekty, prostředky, oddělení, nákladová střediska a geografické oblasti. Vedení používá objekty nákladů, aby mohlo kvantifikovat náklady a také provést analýzu ziskovosti.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Dimenze objektu nákladů a členy dimenze objektu nákladů
Objekty nákladů se označují jako *dimenze objektu nákladů*. Až se rozhodnete, které k jaké osobě by se měl objekt dimenze nákladů vztahovat, musíte zadat jednotlivé hodnoty dimenzí nebo je importovat do nákladového účetnictví z jiných zdrojových systémů. tyto hodnoty jednotlivých dimenzí se nazývají *členy dimenze objektu nákladů*. Chcete například použít finanční dimenzi, které se říká nákladové středisko, jako dimenzi objektu nákladů. Pokud chcete zobrazit, jak náklady míří do jednotlivých nákladových středisek, musíte importovat členy dimenze objektu nákladů. V tomto případě členy dimenze objektu náklady jsou skutečná nákladová střediska, jako například prodej, výroba, administrativa a geografická umístění. Následující obrázek znázorňuje příklad nákladového střediska jako dimenze objektu nákladů s jeho aktuálními nákladovými středisky jako členy dimenze objektu nákladů. 

[![Dimenze objektu nákladů](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Import členů dimenze objektu nákladů pomocí datových konektorů
Ve snaze usnadnit import členů dimenze objektů nákladů používáte datové spojnicemi konektory, abyste mohli načíst hodnoty z osob, které mají být použity jako dimenze objektu nákladů. Můžete použít buď předem připravené datové konektory nebo vlastní datové konektory, které vytvoříte.




