---
title: "Nastavení zabezpečení pro obsah Power BI analýzy nákladového účetnictví"
description: "Toto téma vysvětluje, jak můžete rozšířit zabezpečení na úrovni přístupu v nákladovém účetnictví na zabezpečení na úrovni řádku v aplikaci Microsoft Power BI. Tato funkce pomáhá zajistit, aby uživatelé viděli pouze Power BI data, ke kterým mají udělen přístup."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 04f8cb1a6375be9371bca2af7e4044392ce7322b
ms.openlocfilehash: 12fd8e11211b701304f9f4a68ff31f3b42e3e8ee
ms.contentlocale: cs-cz
ms.lasthandoff: 08/02/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Nastavení zabezpečení pro obsah Power BI analýzy nákladového účetnictví

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak můžete rozšířit zabezpečení na úrovni přístupu v nákladovém účetnictví na zabezpečení na úrovni řádku v aplikaci Microsoft Power BI. Tato funkce pomáhá zajistit, aby uživatelé viděli pouze Power BI data, ke kterým mají udělen přístup.

<a name="overview"></a>Přehled
--------

Obsah **Analýza nákladového účetnictví** v Microsoft Power BI používá Power BI zabezpečení na úrovni řádku k omezení přístupu uživatelů. Zabezpečení je založeno na organizační hierarchii úrovně přístupu, která je nastavena v parametrech nákladového účetnictví. Další informace o obsahu **Analýza nákladového účetnictví** v Power BI najdete v tématu [Obsah analýzy nákladového účetnictví v Power BI](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Nastavení
Chcete-li rozšířit Power BI o zabezpečení na úrovni přístupu, musí vlastník obsahu Power BI postupovat podle následujících kroků. **Poznámka:** Uživatel, který publikuje obsah **Analýzy nákladového účetnictví** v Power BI se automaticky stane vlastníkem. Pouze vlastník může nastavit zabezpečení v Power BI. Navíc dokud vlastník nepřidá další uživatele na PowerBI.com, nikdo kromě vlastníka nemůže zobrazit jakákoliv data v obsahu **Analýzy nákladového účetnictví** v Power BI.

1.  Publikujte soubor definice do Power BI.
2.  Přihlaste se k PowerBI.com.
3.  Vyhledejte soubor dat pro obsah **Analýzy nákladového účetnictví** v Power BI.
4.  Otevřete stránku zabezpečení. 

    ![Otevření stránky zabezpečení](./media/CA-picture-1.png)

5.  Role **Kontrolor objektu nákladů** role je již vytvořena. Přidejte další členy, kteří jsou součástí organizační hierarchie na úrovni přístupu pro nákladové účetnictví. 

    ![Přidání členů](./media/CA-picture-2.png)

Uživatelé, kteří jsou přidáni do role **Kontrolor objektu nákladů** uvidí pouze data, která mohou vidět, podle definice v organizační hierarchii úrovně přístupu nákladového účetnictví. **Poznámka:** Zabezpečení na úrovni řádku platí pro dlaždice a sestavy v aplikaci Microsoft Dynamics 365 for Finance and Operations, které jsou vloženy z Power BI.

## <a name="updating-security"></a>Aktualizace zabezpečení
Pokud provedete aktualizace zabezpečení na úrovni přístupu v nákladovém účetnictví a chcete, aby Power BI odráželo tyto aktualizace, je nutné aktualizovat úložiště entit pro obsah **Analýzy nákladového účetnictví** v Power BI. Po dokončení aktualizace úložiště entit z aplikace Finance and Operations je nutné aktualizovat artefakty na stránkách PowerBI.com. Další informace o postupu aktualizace úložiště entit naleznete v tématu [Aktualizace úložiště entit](power-bi-integration-entity-store.md#update-entity-store). Vlastník obsahu **Analýzy nákladového účetnictví** v Power BI musí také provést aktualizaci úložiště entit, je-li novým uživatelům udělen přístup k organizační hierarchii. Navíc musí vlastník přidat nové uživatele do role **Kontrolor objektu nákladů** roli na PowerBI.com, aby se na ně vztahovalo zabezpečení na úrovni řádku.

## <a name="disabling-security"></a>Zakázání zabezpečení
Předpokládáme, že vaše organizace chce omezit přístup k datům. Pokud jsou z nějakého důvodu parametry zabezpečení zakázány, pokud spustíte nákladové účetnictví, musí vlastník místo toho přidat uživatele do role **Nákladový účetní** v Power BI. Pokud změníte zabezpečení ze stavu povoleno na stav zakázáno, je vhodné odebrat uživatele z role **Kontrolor objektu nákladů**. A naopak, pokud znovu zabezpečení povolíte. Uživatelé mohou patřit k oběma rolím. Společný přístup je spojení obou rolí. U případě obsahu **Analýzy nákladového účetnictví** v Power BI mají uživatelé, kteří mají společný přístup, neomezený přístup k datům. Chcete-li použít omezený přístup, uživatelé musí být přiřazeni pouze k roli **Kontrolor objektu nákladů**. Tyto aktualizace zabezpečení na úrovni řádku se projeví okamžitě. Příslušní uživatele by měli obnovit zobrazení prohlížeče.

## <a name="additional-resources"></a>Další prostředky
Další informace o zabezpečení na úrovni řádku v Power BI naleznete v tématu [Správa zabezpečení na vašem modelu v Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).




