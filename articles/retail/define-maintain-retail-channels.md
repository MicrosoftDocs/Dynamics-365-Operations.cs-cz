---
title: "Definování a udržování maloobchodní sítě"
description: "V tomto článku je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Microsoft Dynamics 365 for Retail označují jako maloobchody. Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení maloobchodu."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 3f0b566963574569cb40b72550e2337c9ba8a2ce
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017

---

# <a name="define-and-maintain-retail-channels"></a>Definování a udržování maloobchodní sítě

[!include[banner](includes/banner.md)]


V tomto článku je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Microsoft Dynamics 365 for Retail označují jako maloobchody. Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení maloobchodu.

Dynamics 365 for Retail podporuje více maloobchodních sítí, jako např. online obchody, kontaktní střediska a kamenné obchody. Kamenný obchod se nazývá maloobchod. Každý maloobchod může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance. Všechny tyto prvky je třeba nastavit pro maloobchod před jeho vytvořením. Po vytvoření maloobchodu přiřadíte produkty, které má obchod obsahovat. K obchodu můžete také přiřadit zaměstnance, pokladny a odběratele. Nakonec přidejte nový obchod do organizační hierarchie.

## <a name="setting-up-retail-stores"></a>Nastavení maloobchodů
Před nastavením maloobchodu v aplikaci Microsoft Dynamics 365 for Retail je nutné dokončit některé předpoklady. Poté můžete vytvořit maloobchod a přidat podrobné informace.

### <a name="prerequisites"></a>Požadavky

Před nastavením maloobchodu je nutné dokončit následující úkoly:

1.  Nastavte organizační strukturu a upravte nastavení organizační hierarchie pro sortiment, doplnění a vykazování maloobchodu.
2.  Vytvořte sklad, který bude maloobchod představovat.
3.  Nastavte číselné řady pro maloobchod, příkazy obchodu a doklady výkazu obchodu.
4.  Konfigurujte parametry pro maloobchod.
5.  Nastavení metody platby, kterou obchod přijímá.
6.  Pro zpracování transakcí platebních karet v maloobchodním pokladním místě (POS) můžete také nastavit platební služby.
7.  Nastavení skupin DPH.
8.  Nastavení maloobchodních produktů. V rámci této úlohy můžete také nastavit hierarchie maloobchodních produktů, varianty produktu a sortiment produktů.
9.  Nastavení cenových skupin výrobků.
10. Nastavení tvorby cen maloobchodních produktů. V rámci této úlohy můžete také nastavit úpravy cen, slevy a období slevy.
11. Nastavení zaměstnanců. **Poznámka:** Je nutné také přiřadit příslušná oprávnění zaměstnancům, aby se mohli přihlásit a provést úlohy pomocí aplikace Dynamics 365 for Retail pro systém Retail POS.
12. Konfigurace profilů Retail POS pro přiřazení k obchodu. Tato úloha zahrnuje mnoho dalších úloh, například nastavení pokladny, nastavení profilu offline a nastavení formátů a profilů účtenky.

Zobrazte všechny úkoly, které jsou zahrnuty v předpokladech, a dokončete pouze úlohy, které se vás týkají.

### <a name="set-up-a-retail-store"></a>Nastavení maloobchodní prodejny

Po dokončení požadovaných úloh dokončete tyto úlohy a nastavte tak podrobné informace o maloobchodě:

1.  Vytvoření maloobchodu.
2.  Přiřazení skupiny DPH k obchodu.
3.  Přiřazení způsobů plateb přijímaných v obchodě.
4.  Přidejte podrobnosti do popisu produktu u produktů nabízených ve vašem maloobchodě. Můžete například přidat formátovaný text a obrázky. Tyto podrobnosti k produktu se zobrazují v různých kontextech, například v pokladně POS nebo na vytištěných štítcích.
5.  Přidejte obchod do výchozí organizační hierarchie, která je přiřazena k účelu **Maloobchodní sortiment**, **Doplnění maloobchodu** nebo **Vykazování maloobchodu**.

### <a name="after-you-set-up-a-retail-store"></a>Po nastavení maloobchodu

Po zadání podrobností pro maloobchod dokončete tyto úlohy a odešlete nová data maloobchodu do Retail POS:

1.  Nastavte pokladny POS pro obchod.
2.  Přiřazení sortimentů produktů k obchodu.
3.  Zpracujte sortiment, vytvořte seznam produktů, které jsou zahrnuty v sortimentu a zpřístupněte produkty v maloobchodu.
4.  Odešlete data, jako číselné řady, profily hardwaru a rozložení obrazovky POS, do pokladen Retail POS.
5.  Publikujte maloobchod a odešlete tak data obchodu do Retail POS.
6.  Spusťte úlohy a odešlete data obchodu do Retail POS.

## <a name="organization-hierarchies"></a>Organizační hierarchie
Retail používá hierarchie organizace pro potřeby strukturování maloobchodních kanálů. Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik. Při nastavování obchodů je můžete přidat do organizační hierarchie. Obchody poté budou sdílet data, která se používají pro sortimenty, doplnění a vykazování.




