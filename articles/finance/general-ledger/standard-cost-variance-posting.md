---
title: Účtování standardní odchylky nákladů
description: Tento článek poskytuje informace o nastavení profilů účtování pro standardní kalkulaci.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: e7b2d04f32b75dbd1354b3ef74a41ea1b6469c8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894870"
---
# <a name="standard-cost-variance-posting"></a>Účtování standardní odchylky nákladů

Když používáte standardní kalkulaci u jednoho nebo více produktů ve vaší organizaci, musíte konfigurovat [předpoklady pro standardní kalkulaci](/supply-chain/cost-management/prerequisites-standard-costs.md). Tento článek vysvětluje účty pro zaúčtování, které jsou vyžadovány pro krok 3 předpokladů, „Přiřazení účtů hlavní knihy k účtování položek, které souvisejí se standardními odchylkami nákladů“.

U nákupních objednávek a výrobních zakázek mohou nastat různé typy odchylek. Příklady výrobních odchylek najdete v tématu [Běžné zdroje výrobních odchylek](/supply-chain/cost-management/common-sources-of-production-variances.md). K odchylkám v ceně nákupní objednávky dochází, když pro zakoupenou položku použijete standardní cenu a existuje rozdíl mezi standardní cenou produktu a fakturovanou částkou v nákupní objednávce.

## <a name="sample-posting-profile-configuration"></a>Ukázka konfigurace profilu zveřejňování

Následující tabulka ukazuje příklady výchozích typů účtování. Zahrnuje ukázkové hlavní účty a popisy.

- Sloupec „Debetní/kreditní?“ udává, zda je transakce obvykle debetní nebo kreditní. V určitém případě může transakce zaúčtovat buď debety, nebo kredity.
- Sloupec „Clearingový účet“ označuje, že typ účtování je clearingový účet. To znamená, že částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce.
- Sloupec "P/F" označuje typ účtování. „P“ představuje fyzické účtování a „F“ představuje finanční účtování.
- Sloupec „Sledovat“ udává, zda je hlavní účet pro typ účtování obvykle stejný jako hlavní účet pro jiný typ účtování. Konkrétně označuje typ účtování, který se obvykle používá.

> [!NOTE]
> Hlavní účty a názvy hlavních účtů v tabulce jsou pouze návrhy. Doporučujeme, abyste ve spolupráci se svým účetním určili nejlepší konfiguraci pro vaše obchodní potřeby.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | P/F | Sledovat | Popis |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Odchylka nákupní ceny | 510310 | Odchylka nákupní ceny | Výdaje | kterýkoli | Číslo | F | Nelze použít | Tento účet se používá, když existuje rozdíl mezi nákupní cenou a standardní cenou na nákupní objednávce. |
| Přecenění nákladu skladu | 510330 | Přecenění nákladu skladu | Výdaje | kterýkoli | Číslo | F | Nelze použít | Tento účet se používá, když je aktivována nová verze kalkulace pro standardní nákladovou položku k přecenění skladových zásob. |
| Odchylka změny nákladů | 510320 | Odchylka změny nákladů | Výdaje | kterýkoli | Číslo | F | Nelze použít | Tento účet se používá, když existuje rozdíl ve standardních nákladech mezi místy nebo když je položka vrácena a dojde ke změně mezi původní standardní cenou a aktuální standardní cenou produktu. |
| Výrobní odchylka velikosti šarže | 510370 | Výrobní odchylka velikosti šarže | Výdaje | kterýkoli | Číslo | F | Nelze použít | Tento účet se používá, když existují rozdíly mezi základem výpočtu kusovníku a skutečným množstvím pro výpočet nákladů na výrobní zakázku. |
| Odchylka výrobní ceny | 510340 | Odchylka výrobní ceny | Výdaje | kterýkoli | Číslo | F | Nelze použít | Tento účet se používá, když existují cenové rozdíly mezi odhadovanými náklady a skutečnými náklady na výrobní zakázku. |
| Odchylka výrobního množství | 510350 | Odchylka výrobního množství | Výdaje | kterýkoli | Číslo | F | Nelze použít | Tento účet se používá, když existují množstevní rozdíly mezi odhadovanými náklady a skutečnými náklady na výrobní zakázku. |
| Odchylka výrobní náhrady | 510360 | Odchylka výrobní náhrady | Výdaje | kterýkoli | Číslo | F | Nelze použít | Tento účet se používá v případě neočekávané spotřeby na výrobní zakázce. |
| Odchylka zaokrouhlení | 618160 | Rozdíly zaokrouhlení | Výdaje | kterýkoli | Číslo | F | Nelze použít | Tento účet se používá, když dojde k zaokrouhlovacímu rozdílu při výpočtu výrobních nákladů ze standardních nákladů. |
