---
title: Vytvořit právnické osoby
description: Toto téma popisuje, jak vytvořit právnické osoby v Microsoft Dynamics 365 Commerce, které je nutné před vytvořením kanálů vytvořit a nakonfigurovat.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9491feb004366a02155225bfb323773e130f3dc9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993596"
---
# <a name="create-legal-entities"></a>Vytvořit právnické osoby


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvořit právnické osoby v Microsoft Dynamics 365 Commerce, které je nutné před vytvořením kanálů vytvořit a nakonfigurovat.

## <a name="overview"></a>Přehled

Právnická osoba je organizace, která má registrovanou nebo uzákoněnou právní strukturu. Právnické osoby mohou uzavírat právní smlouvy a je po nich vyžadována příprava výkazů s informacemi o jejich výkonu.

Společnost je typ právnické osoby. V současné době jsou společnosti pouze druhem právnické osoby, kterou můžete vytvořit, a každá právnická osoba je spojena s identifikátorem společnosti. Toto přiřazení existuje vzhledem k tomu, že některé funkční oblasti v aplikaci používají ID společnosti nebo *DataAreaId* ve svých datových modelech. V těchto funkčních oblastech jsou společnosti používány jako hranice pro zabezpečení dat. Uživatelé mohou přistupovat k datům pouze pro společnost, ke které jsou aktuálně přihlášeni. 

Při vytváření kanálu je nutné určit právnickou osobu, ke které daný kanál náleží.

## <a name="create-a-new-legal-entity"></a>Vytvořit novou právnickou osobu

Chcete-li vytvořit novou právnickou osobu v Dynamics 365 Commerce, postupujte následovně.

1. V navigačním podokně přejděte na **Moduly \> Nastavení centrály \> Právnické osoby**.
1. V podokně akcí zvolte **Nový**. Vpravo sezobrazí podokno **Nová právnická osoba**.
1. Zadejte hodnotu do pole **Název**.
1. Do pole **Společnost** zadejte hodnotu.
1. V poli **Země/oblast** zadejte nebo vyberte hodnotu.
1. Vyberte **OK**. 

   ![Vytvoření právnické osoby](media/legal-entities.png)

1. V sekci **Obecné** zadejte následující obecné informace o právnické odobě: 
   1. Pokud je požadován vyhledávací název, zadejte vyhledávací název. Vyhledávací název je alternativní název, který lze použít k hledání tohoto právního subjektu. 
   1. Vyberte, zda je tato právnická osoba používána jako konsolidační společnost.
   1. Vyberte, zda je tato právnická osoba používána jako eliminační společnost. 
   1. Vyberte **výchozí jazyk** pro entitu. 
   1. Vyberte **časové pásmo** pro entitu.
1. V části **Adresy** vyberte **Upravit** a zadejte údaje adresy, například název ulice, číslo, PSČ a město.
1. V části **Kontaktní informace** zadejte informace o metodách komunikace, například e-mailové adresy, adresy URL a telefonní čísla.
1. V části **Statutární vykazování** zadejte registrační čísla, která se používají pro statutární vykazování.
1. V části **Registrační čísla** zadejte informace vyžadované právnickou osobou.
1. V části **Informace o bankovním účtu** zadejte bankovní účty a směrové kódy pro právnickou osobu.
1. V části **Zahraniční obchod a logistika** zadejte dodací informace pro právnickou osobu.
1. V části **Číselné řady** můžete zobrazit číselné řady, které jsou spojeny s právním subjektem. Tato možnost bude prázdná, aby začínala hodnotou.
1. V části **Obrázek řídicího panelu** můžete zobrazit nebo změnit obrázek loga a/nebo řídicího panelu přidružený k právnické osobě.
1. V části **Daňová registrace** zadejte registrační čísla, která se používají při styku s finančními úřady.
1. V části **Daň 1099** zadejte informace 1099 pro právní subjekt.
1. V části **Daňové informace** zadejte daňové informace pro právnickou osobu.
1. Zvolte **Uložit**.

Na následujícím obrázku je podrobný příklad právnické osoby.

![Obecná část právnické osoby](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Další zdroje

[Přehled organizací a organizačních hierarchií](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Plánování organizační hierarchie](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organizační hierarchie](channels-org-hierarchies.md)

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)
