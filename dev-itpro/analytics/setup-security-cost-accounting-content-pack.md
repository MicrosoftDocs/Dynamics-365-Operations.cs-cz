---
title: "Nastavení zabezpečení pro analýzu obsahu Power BI nákladového účetnictví"
description: "Toto téma vysvětluje, jak můžete rozšířit zabezpečení úroveň přístupu v nákladovém účetnictví pro řádek úroveň zabezpečení v aplikaci Microsoft Power BI. Tato funkce pomáhá zajistit, aby uživatelé viděli pouze data BI napájení, které je udělen přístup k."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Nastavení zabezpečení pro analýzu obsahu Power BI nákladového účetnictví

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak můžete rozšířit zabezpečení úroveň přístupu v nákladovém účetnictví pro řádek úroveň zabezpečení v aplikaci Microsoft Power BI. Tato funkce pomáhá zajistit, aby uživatelé viděli pouze data BI napájení, které je udělen přístup k.

<a name="overview"></a>Přehled
--------

**Analýzy nákladového účetnictví** obsah Microsoft Power BI můžete omezit přístup uživatele používá zabezpečení na úrovni řádku Power BI. Zabezpečení je založeno na hierarchii organizační úroveň přístupu, která je nastavena v parametry nákladového účetnictví. Další informace o **analýzy nákladového účetnictví** obsahu, viz Power BI [nákladového účetnictví analýzy obsahu Power BI](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Nastavení
Chcete-li rozšířit zabezpečení úroveň přístupu k Power BI, musí vlastník obsahu Power BI postupujte takto. **Poznámka:** uživatel, který publikuje **analýzy nákladového účetnictví** obsahu Power BI automaticky stane vlastníkem. Pouze vlastník může nastavit zabezpečení v Power BI. Navíc dokud vlastník přidá ostatním uživatelům na PowerBI.com, nikdo kromě vlastníka můžete zobrazit všechna data v **analýzy nákladového účetnictví** obsahu Power BI.

1.  Publikujte soubor definice Power BI.
2.  Přihlásit se k PowerBI.com.
3.  Najít datové sady pro **analýzy nákladového účetnictví** obsahu Power BI.
4.  Otevřete stránku zabezpečení. 

    [![Otevřete stránku zabezpečení](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  **Cena objektu řadiče** role je již vytvořena. Přidáte další členy, kteří jsou součástí nákladového účetnictví organizační hierarchii úroveň přístupu. 

    [![Přidání členů](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Uživatelé, kteří jsou přidáni do **cena objektu řadiče** roli uvidí pouze data, která mohou vidět, podle definice v organizační hierarchii úroveň přístupu nákladového účetnictví. **Poznámka:** zabezpečení na úrovni řádku platí pro dlaždice a sestavy v Microsoft Dynamics 365 pro operace, které jsou vloženy v Power BI.

## <a name="updating-security"></a>Aktualizace zabezpečení
Aktualizace provedené v zabezpečení úrovně přístupu v nákladovém účetnictví a vy chcete BI napájení tak, aby odrážely tyto aktualizace, je nutné aktualizovat úložiště entita pro **analýzy nákladového účetnictví** obsahu Power BI. Po dokončení aktualizace úložiště entita z 365 Dynamics pro operace, je nutné aktualizovat artefakty na PowerBI.com. Další informace o postupu aktualizace entity úložiště naleznete v tématu [úložiště entita aktualizace](power-bi-integration-entity-store.md#update-entity-store). Vlastník **analýzy nákladového účetnictví** obsahu Power BI také nutné provést aktualizaci úložiště entita, je-li novým uživatelům jsou udělena přístupová práva k organizační hierarchii. Navíc musí vlastník přidání nových uživatelů do **cena objektu řadiče** roli na PowerBI.com, takže tento řádek úroveň zabezpečení platí pro ně.

## <a name="disabling-security"></a>Zakázání zabezpečení
Předpokládáme, že vaše organizace chce omezit přístup k datům. Pokud z nějakého důvodu parametry zabezpečení jsou zakázány, pokud spustíte nákladového účetnictví, musí vlastník přidat uživatele **účetní náklady** role v Power BI místo. Pokud změníte zabezpečení z povoleného stavu zakázána, je vhodné odebrat uživatele ze **cena objektu řadiče** roli. A naopak, pokud znovu povolit zabezpečení. Uživatelé mohou patřit k oběma rolím. Společný přístup je unie obě role. U **analýzy nákladového účetnictví** Power BI obsahu uživatelům, kteří mají společný přístup mají neomezený přístup k datům. Chcete-li použít s omezeným přístupem, je-li uživatelům musí být přiřazena pouze **náklady objektu řadiče** role. Tyto aktualizace zabezpečení na úrovni řádku se projeví okamžitě. Příslušné uživatele by mělo obnovit zobrazení prohlížeče.

## <a name="additional-resources"></a>Další prostředky
Další informace o zabezpečení na úrovni řádku BI napájení, viz [spravovat zabezpečení v modelu v Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).




