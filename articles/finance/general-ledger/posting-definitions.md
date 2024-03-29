---
title: Definice účtování
description: Tento článek obsahuje informace o definicích účtování a o tom, jak je lze definovat a propojit. U podporovaných typů zaúčtování a dokumentů můžete ke klasifikaci hlavních účtů a finančních dimenzí účetních položek použít namísto účetních profilů definice účtování.
author: kweekley
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f60506e039623ae7a97f6b4e835f751da15ac0c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898142"
---
# <a name="posting-definitions"></a>Definice účtování

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o definicích účtování a o tom, jak je lze definovat a propojit.
U podporovaných typů zaúčtování a dokumentů můžete ke klasifikaci hlavních účtů a finančních dimenzí účetních položek použít namísto účetních profilů definice účtování. Podporované dokumenty a typy účtování můžete prohlížet na stránce **Definice účtování transakcí**. 

Chcete-li začít definice účtování používat, vyberte možnost **Použít definice účtování** na stránce **Parametry hlavní knihy**. I když použijete definice účtování, stále je nutné definovat účetní profily pro původní položky a nepodporované typy zaúčtování a dokumentů. 

Definice účtování musíte použít, abyste umožnili účtování břemen pro nákupní objednávky a účtování předběžných břemen pro nákupní požadavky.

## <a name="defining-posting-definitions"></a>Definování definic účtování
Použijte stránku **Definice účtování** k určení kritérií shody a definování položek, které by se měly generovat, pokud dojde ke shodě. Kritéria shody se posuzují pro původní položky jako rozúčtování. 

Na stránce **Definice účtování** můžete také řádkům položek přiřadit čísla priorit, abyste mohli řídit pořadí, v jakém se řádky posuzují. Řádky, které mají nejnižší číslo priority, se vyhodnocují jako první. Příklad: posoudí se všechny řádky, které mají prioritu 1, poté řádky, které mají prioritu 2, a tak dále. Při zjištění shody jsou ostatní kritéria párování ignorována. Pouze kritéria ve skupině, která odpovídá původní transakci, vytvářejí generované položky. 

Definice účtování můžete ověřit pomocí **Průvodce definicí účtování (testu)**. Po definování vzorové původní položky pro definici účtování se zobrazí generované položky. 

Verze definic účtování můžete použít spolu s daty účinnosti. Na příklad můžete vytvořit příští verzi definice účtování k účtování jiného účtu hlavní knihy v novém fiskálním roce. 

Použijte stránku **Definice účtování transakcí** pro přiřazení účtovacích definic k typům transakcí.

## <a name="linking-posting-definitions"></a>Propojení definic účtování
Při vytváření účtovacích definic můžete propojit jednu účtovací definici s jinou. Kritéria definice, s kterou propojujete, se považují za rozšíření kritérií aktuální definice účtování. Tato funkce pomáhá ušetřit čas, protože pro aktuální definice účtování není nutné znovu zadat kritéria na pevné záložce **Položky** na stránce **Definice účtování**, pokud jste již řádky zadali pro jinou definici. 

Do diagramů nebo tabulek zahrňte všechny odkazy, které byste mohli použít. Abyste zabránili konfliktům s aktuální definicí účtování, ujistěte se, že všechny řádky v definicích účtování, s kterými propojujete, jsou jedinečné. 

Tato omezení platí v případě, že vytvoříte odkazy v definicích účtování:

-   Konkrétní definice účtování může buď odkazovat na jinou definici účtování, nebo může jiná definice účtování odkazovat na ni, ale nemohou nastat obě situace zároveň. Definice účtování ovšem může odkazovat na více definic účtování.
-   Odkazy můžete nastavit pouze mezi definicemi účtování, které jsou ve stejném modulu.
-   Definici účtování můžete přiřadit k libovolnému typu transakce, ale tento typ transakce musí být ve stejném modulu jako definice účtování. Použijte stránku **Definice účtování transakcí** a podívejte se, v kterém modulu typ transakce je.


Další informace získáte v části [Příklady definice účtování](example-posting-definitions.md). 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
