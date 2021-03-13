---
title: Přizpůsobení transakčních e-mailů podle způsobu doručení
description: Toto téma popisuje, jak nastavit vlastní e-mailové šablony pro konkrétní typy oznámení a způsoby doručení v Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: f4ecb990cfe792e92142f922c43c71ef8494e117
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031841"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Přizpůsobení transakčních e-mailů podle způsobu doručení

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak nastavit vlastní e-mailové šablony pro konkrétní typy oznámení a způsoby doručení v Microsoft Dynamics 365 Commerce.

Transakční e-maily lze nyní přizpůsobit pro kombinaci typu oznámení (například **Objednávka byla vytvořena**, **Objednávka byla zabalena** nebo **Objednávka byla fakturována**) a způsobu doručení (například přes noc, vyzvednutí na prodejně nebo pouliční výdej). Vlastní transakční e-maily umožňují maloobchodníkům poskytnout svým zákazníkům objednávku, která je přizpůsobena způsobu jejího doručení. Například událost „objednávka byla zabalena“ lze například přizpůsobit tak, aby poskytovala pokyny pro pouliční výdej pro zákazníky, kteří si jej vybrali. Alternativně může obsahovat přepravce a informace o doručení pro zákazníky, kteří se rozhodnou nechat svou objednávku odeslat.

> [!NOTE]
> Chcete-li použít funkci přizpůsobených transakčních e-mailů, musíte nejprve zapnout funkci **Přizpůsobení šablon transakčních e-mailů podle způsobu doručení** přechodem na **Pracovní prostory \> Správa funkcí** v centrále Commerce.

E-maily lze přizpůsobit podle způsobu doručení pro následující typy oznámení:

- **Objednávka byla stornována** – Tento typ e-mailového oznámení je nový.
- **Objednávka byla vytvořena**
- **Objednávka byla potvrzena.**
- **Objednávka byla fakturována** – Tento typ e-mailového oznámení je nový. Může být použit místo typu oznámení **Objednávka byla poslána**, které odešle oznámení o jakékoli fakturační události, která má expedovaný způsob doručení (nikoli vyzvednutí, vyvezení nebo elektronický způsob doručení).
- **Objednávka byla vyskladněna**
- **Objednávka byla zabalena**
- **Objednávka připravena k vyzvednutí** – Tento typ oznámení lze upravit podle způsobu doručení, pouze pokud je zapnuta funkce **Podpora více způsobů vyzvednutí/doručení**. V takovém případě je tento typ oznámení funkčně ekvivalentní s typem oznámení **Objednávka byla zabalena**.
- **Platba se nezdařila.**
- **Objednávka náhrady byla vytvořena.**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>Konfigurace e-mailových šablon pro konkrétní způsoby doručení

U tohoto postupu se předpokládá, že jste již vytvořili své nové, vlastní e-mailové šablony a přidali je na stránku **E-mailové šablony organizace**. Informace, jak vytvořit a nahrát e-mailové šablony, najdete v části [Vytvoření e-mailových šablon pro transakční události](email-templates-transactions.md).

Chcete-li nakonfigurovat e-mailové šablony pro konkrétní způsoby doručení v centrále Commerce, postupujte takto.

1. Jděte na **Profil e-mailového oznámení Commerce**.
1. Pod **Nastavení maloobchodního oznámení události** vyberte existující typ oznámení.
1. Ponechte vybrán typ oznámení a vyberte **Konfigurace způsobů doručení**.
1. V dialogovém okně **Způsoby doručení** zvolte **Nový**.
1. V novém řádku v poli **Způsob doručení** zvolte způsob doručení.
1. V poli **ID e-mailu** vyberte e-mailovou šablonu, kterou chcete namapovat na způsob doručení.
1. Zaškrtněte políčko **Aktivní**.
1. Opakováním kroků 4 až 7 přidejte další způsoby doručení.
1. Po dokončení zvolte **OK**.

> [!NOTE]
> - Pokud je v prodejní objednávce na řádcích více než jeden způsob doručení, použije se výchozí šablona. Výchozí šablona je šablona, která je namapována na typ oznámení na stránce **Profil e-mailového oznámení Commerce**.
> - Pokud má prodejní objednávka způsob doručení, který nebyl nakonfigurován pro vlastní e-mailovou šablonu, použije se výchozí e-mailová šablona.

## <a name="additional-resources"></a>Další prostředky

[Vytváření objednávek v kontaktním středisku](tasks/create-call-center-orders.md)

[Změna způsobu dodání v POS](pos-change-delivery-mode.md)
