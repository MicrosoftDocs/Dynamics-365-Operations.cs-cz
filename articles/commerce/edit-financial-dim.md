---
title: Úprava finančních dimenzí pro maloobchodní transakce
description: Tento článek popisuje, jak upravit finanční dimenze pro maloobchodní transakce v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: b382907cd79a13319601dd694261319875565947
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268387"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Úprava finančních dimenzí pro maloobchodní transakce

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak upravit finanční dimenze pro maloobchodní transakce v Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>Úprava finančních dimenzí

Chcete-li upravit finanční dimenze pro maloobchodní transakce v Commerce Headquarters, postupujte takto.

1. Otevřete stránku **Konfigurace finanční dimenze pro integraci aplikací**.
1. Vyberte aktivní záznam **Výchozí integrace dimenzí**.
1. Na záložce s náhledem **Finanční dimenze** se ujistěte, že všechny dimenze, které chcete upravit v listu aplikace Excel, jsou přítomny v seznamu **Vybrané**. Další informace viz [Datové entity](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).
1. Stáhněte a otevřete soubor Excel ze stránky **Výkazy**, stránky **Maloobchodní transakce** nebo dlaždice **Selhání ověření transakcí** v pracovním prostoru **Finance obchodu**.
1. Chcete-li změnit finanční dimenzi transakce, vyberte **Návrh** a potom vyberte symbol tužky vedle řádku **Transakce (auditovatelná)**.
1. Najděte a vyberte pole **FinancialDimensionDisplayValue**, vyberte buňku v části záhlaví listu aplikace Excel a poté vyberte **Přidat popisek**.
1. Vyberte buňku pod buňkou, kterou jste vybrali v předchozím kroku, vyberte **Přidat hodnotu** a potom vyberte **Obnovit**. Finanční dimenze jsou přidány do listu aplikace Excel a poté je lze upravit a publikovat.
1. Chcete-li změnit dimenze na řádcích transakce, vyberte řádek **Prodejní transakce (auditovatelné)**, vyberte symbol tužky a opakujte kroky 6 a 7.
1. Chcete-li změnit dimenze na řádcích platby, vyberte řádek **Platební transakce (auditovatelné)**, vyberte symbol tužky a opakujte kroky 6 a 7.

## <a name="additional-resources"></a>Další zdroje

[Úpravy a audit transakcí cash and carry a řízení hotovosti](edit-cash-trans.md)

[Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků](edit-order-trans.md)

[Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí](create-excel-edit.md)

[Přidání polí do sešitu aplikace Excel pro úpravu maloobchodních transakcí](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
