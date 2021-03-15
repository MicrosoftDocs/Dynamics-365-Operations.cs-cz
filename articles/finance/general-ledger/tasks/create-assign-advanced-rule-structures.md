---
title: Vytvoření a přiřazení struktur rozšířeného pravidla
description: Toto téma vysvětluje, jak vytvořit pokročilou strukturu pravidel a přiřadit ji k účetní struktuře.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6a3f7d174c91e357dce8a19ab50a5cd42a85561
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968586"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Vytvoření a přiřazení struktur rozšířeného pravidla

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit pokročilou strukturu pravidel a přiřadit ji k účetní struktuře. Tento průvodce používá ukázkovou společnost USMF.

## <a name="create-an-advanced-rule-structure"></a>Vytvořit strukturu rozšířeného pravidla
1. Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Účetní osnovy > Struktury > Pokročilé struktury pravidel**.
2. Kliknutím na možnost **Nový** otevřete dialogové okno.
3. V poli **Rozšířené struktury pravidel** zadejte název k popisu struktury pravidla.
4. Vyberte **OK**.
5. Vyberte **Přidat segment**.
6. V seznamu segmentů vyberte finanční dimenzi. Například **Obchod**.  
7. Vyberte **Přidat segment**.
8. Vyberte **Aktivovat**.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Použití struktury rozšířeného pravidla na účetní strukturu
1. Přejděte na **navigační podokno > Moduly > Hlavní kniha > Účetní osnovy > Struktury > Konfigurovat účetní struktury**.
2. V seznamu vyhledejte a vyberte účetní struktury, na které chcete uplatnit rozšířené pravidlo.
3. Vyberte možnost **Upravit**. Můžete také vybrat **Pokročilá pravidla** a budete vyzváni vložit účetní strukturu v **režimu konceptu**.  
4. Vyberte **Upřesnit pravidla**.
5. Kliknutím na možnost **Nový** otevřete dialogové okno.
6. Zadejte hodnotu do pole **Upřesnit pravidlo**.
7. Zadejte hodnotu do pole **Název**.
8. Vyberte **Vytvořit**.
9. Vyberte **Přidat nová kritéria**.
10. V poli **Kde** vyberte hlavní účet nebo finanční dimenzi.
11. V poli **Operátor** vyberte možnost, jako **je mezi** a **zahrnuje**.
12. Zadejte hodnotu do pole **Hodnota**.
13. Zadejte hodnotu do pole **prostřednictvím**.
14. Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.
15. V seznamu vyhledejte pokročilé pravidlo, které chcete použít, když jsou splněna zadaná kritéria.
16. Vyberte **přidat**.
17. Zavřete stránku.
18. Vyberte **Aktivovat**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]