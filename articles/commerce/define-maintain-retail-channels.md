---
title: Definování a udržování maloobchodní sítě
description: V tomto tématu je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Dynamics 365 Commerce označují jako obchody. Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení obchodu.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410700"
---
# <a name="define-and-maintain-retail-channels"></a>Definování a udržování maloobchodní sítě

[!include [banner](includes/banner.md)]

V tomto tématu je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Dynamics 365 Commerce označují jako obchody. Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení obchodu.

Commerce podporuje více obchodních sítí, jako například online obchody, kontaktní střediska a kamenné obchody. Kamenný obchod se nazývá obchod. Každý obchod může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance. Všechny tyto prvky je třeba nastavit pro obchod před jeho vytvořením. Po vytvoření obchodu přiřadíte produkty, které má obchod obsahovat. K obchodu můžete také přiřadit zaměstnance, pokladny a odběratele. Nakonec přidejte nový obchod do organizační hierarchie.

## <a name="setting-up-stores"></a>Nastavení obchodů

Před nastavením maloobchodu v Commerce je nutné dokončit některé předpoklady. Poté můžete vytvořit obchod a přidat podrobné informace.

### <a name="prerequisites"></a>Předpoklady

Před nastavením obchodu je nutné dokončit následující úkoly:

1. Nastavte organizační strukturu a upravte nastavení organizační hierarchie pro sortiment, doplnění a vykazování maloobchodu.
2. Vytvořte sklad, který bude obchod představovat.
3. Nastavte číselné řady pro obchod, příkazy obchodu a doklady výkazu obchodu.
4. Konfigurovat parametry pro Commerce.
5. Nastavení metody platby, kterou obchod přijímá.
6. Pro zpracování transakcí platebních karet v pokladním místě (POS) můžete také nastavit platební služby.
7. Nastavení skupin DPH.
8. Nastavení produktů. V rámci této úlohy můžete také nastavit hierarchie obchodních produktů, varianty produktu a sortiment produktů.
9. Nastavení cenových skupin výrobků.
10. Nastavit ceny produktu. V rámci této úlohy můžete také nastavit úpravy cen, slevy a období slevy.
11. Nastavení zaměstnanců.

    > [!NOTE]
    > Poznámka: Je nutné také přiřadit příslušná oprávnění zaměstnancům, aby se mohli přihlásit a provést úlohy pomocí systému POS.

12. Konfigurace profilů POS pro přiřazení k obchodu. Tato úloha zahrnuje mnoho dalších úloh, například nastavení pokladny, nastavení profilu offline a nastavení formátů a profilů účtenky.

Zobrazte všechny úkoly, které jsou zahrnuty v předpokladech, a dokončete pouze úlohy, které se vás týkají.

### <a name="set-up-a-store"></a>Nastavit obchod

Po dokončení požadovaných úloh dokončete tyto úlohy a nastavte tak podrobné informace o obchodě:

1. Vytvoření obchodu.
2. Přiřazení skupiny DPH k obchodu.
3. Přiřazení způsobů plateb přijímaných v obchodě.
4. Přidejte podrobnosti do popisu produktu u produktů nabízených ve vašich obchodech. Můžete například přidat formátovaný text a obrázky. Tyto podrobnosti k produktu se zobrazují v různých kontextech, například v pokladně POS nebo na vytištěných štítcích.
5. Přidejte obchod do výchozí organizační hierarchie, která je přiřazena k účelu **Maloobchodní sortiment**, **Doplnění maloobchodu** nebo **Vykazování maloobchodu**.

### <a name="after-you-set-up-a-store"></a>Po nastavení obchodu

Po zadání podrobností pro obchod dokončete tyto úlohy a odešlete nová data obchodu do POS:

1. Nastavte pokladny POS pro obchod.
2. Přiřazení sortimentů produktů k obchodu.
3. Zpracujte sortiment, vytvořte seznam produktů, které jsou zahrnuty v sortimentu a zpřístupněte produkty v obchodu.
4. Odešlete data, jako číselné řady, profily hardwaru a rozložení obrazovky POS, do pokladen POS.
5. Publikujte obchod a odešlete tak data obchodu do POS.
6. Spusťte úlohu a odešlete tak data obchodu do POS.

## <a name="organization-hierarchies"></a>Organizační hierarchie

Commerce používá hierarchie organizace pro potřeby strukturování obchodních kanálů. Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik. Při nastavování obchodů je můžete přidat do organizační hierarchie. Obchody poté budou sdílet data, která se používají pro sortimenty, doplnění a vykazování.

> [!NOTE]
> Chcete-li použít funkci Commerce prodeje, je nutné povolit konfigurační klíč **Více dodacích adres**. Tento konfigurační klíč je k dispozici v klíčích **Obchodní konfigurace** ve složce **Správa systému**\> **Nastavení** \> **Konfigurace licence**. To je vyžadováno z důvodu různých ověření na základě dodací adresy nakonfigurované na úrovni řádku prodejní objednávky.



[!INCLUDE[footer-include](../includes/footer-banner.md)]