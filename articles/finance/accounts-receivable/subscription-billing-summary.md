---
title: Přehled fakturace předplatného
description: Tento článek popisuje fakturaci předplatného v aplikaci Microsoft Dynamics 365 Finance.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 10302e9ae7dff3d018897b666caaf4d4289b4866
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856734"
---
# <a name="subscription-billing-overview"></a>Přehled fakturace předplatného

[!include [banner](../includes/banner.md)]

Fakturace předplatného umožňuje organizacím spravovat příležitosti k výnosům z předplatného a opakovaně fakturovat prostřednictvím plánů fakturace. Komplexní cenové a fakturační modely a alokace výnosů se snadno spravují a jsou účtovány a uznávány na úrovni řádku. Víceprvková alokace výnosů umožňuje alokaci výnosů v souladu s mezinárodními účetními normami (International Financial Reporting Standard 15 \[IFRS 15\]) a Obecně uznávanými účetními zásadami ve Spojených státech (US GAAP) (Accounting Standards Codification Topic 606 \[ASC 606\]).

Řešení má tři moduly, které lze používat nezávisle. Alternativně lze všechny tři moduly používat společně.

- **Opakovaná fakturace smlouvy** – Tento modul umožňuje opakovanou fakturaci a správu cen pro zajištění kontroly nad cenami a parametry fakturace, obnovení smlouvy a konsolidované fakturace.
- **Časové rozlišení výnosů a nákladů** – Tento modul eliminuje manuální procesy a závislost na externích systémech tím, že spravuje výnosy a umožňuje přehled o měsíčních opakujících se výnosech v reálném čase.
- **Víceprvkové rozdělení příjmů** – Tento modul pomáhá s dodržováním právních předpisů v oblasti výnosů tím, že zpracovává ceny a rozděluje výnosy mezi více položek.

Další informace o fakturaci předplatného viz [Vyúčtování předplatného obsahu Power BI](sub-bill-power-bi.md).

Fakturace předplatného je povolena prostřednictvím **Správy funkcí**. Nelze ji však použít spolu s funkcí **Uznání výnosů**. Před aktivací fakturace předplatného proto musíte tuto funkci zakázat.

1. V pracovním prostoru **Správa funkcí** zadejte na kartě **Vše** ve filtru **Uznání výnosů** a pak jako filtr vyberte název funkce.
2. Vyberte funkci **Uznání výnosů** a poté vyberte tlačítko **Zakázat**.
3. Ve filtru **Název funkce** zadejte **Fakturace předplatného** a poté vyberte filtr modulu.
4. Vyberte funkci **Fakturace předplatného** a poté vyberte **Povolit**.
5. Vyberte jeden ze tří modulů z předchozího seznamu a poté vyberte **Povolit**. Tento krok opakujte pro oba ostatní moduly.

    > [!IMPORTANT]
    > Funkce **Fakturace předplatného** musí být povolena, než budete moci aktivovat kterýkoli ze tří modulů.
