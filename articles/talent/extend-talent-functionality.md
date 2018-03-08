---
title: "Rozšíření funkce Microsoft Dynamics 365 for Talent"
description: "Pokud jste vytvořili jakoukoliv aplikaci Microsoft PowerApps, můžete spustit tyto aplikace z odkazů v rámci aplikace Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cfd3b475b113fdab4ceeb3e636fea6c9134ab982
ms.openlocfilehash: 0ab829803634871c9060daa381bd02d7d2bbdf42
ms.contentlocale: cs-cz
ms.lasthandoff: 12/01/2017

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Rozšíření funkce Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]

Pokud jste vytvořili jakoukoliv aplikaci Microsoft PowerApps, můžete spustit tyto aplikace z odkazů v rámci aplikace Microsoft Dynamics 365 for Talent. Chcete-li nastavit přístup ke svým aplikacím, musíte nastavit některé informace v aplikaci Talent na stránce konfigurace, kterou lze otevřít z pracovního prostoru **Správa systému**.

## <a name="configuring-embedded-powerapps-within-talent"></a>Konfigurace integrovaných aplikací PowerApps v rámci aplikace Talent
Použijte stránku **Nastavení integrovaných aplikací Microsoft PowerApps** pro konfiguraci stránek Talent slouží ke spuštění aplikací PowerApps. Chcete-li otevřít stránku **Nastavení integrovaných aplikací Microsoft PowerApps**, otevřete pracovní prostor **Správa systému** a potom otevřete kartu **Odkazy**. Zvolte **Microsoft PowerApps** ze skupiny **Nastavení**. 

Na této stránce se zadávají nebo nastavují následující informace: 

> - Popisný název nebo identifikátor pro každou aplikaci PowerApps.
> - Jedinečný identifikátor (GUID) pro každou aplikaci přidanou na stránku Talent. ID aplikace je k dispozici na webu PowerApps [powerapps.com](http://powerapps.com/). 
> - Stránka, odkud mohou uživatelé otevřít aplikaci nebo sestavu. Ne všechny stránky Talent podporují integrované aplikace PowerApps a sestavy Power BI. 

 > [!NOTE]
 >  Zadejte interní název stránky, nikoli zobrazovaný název, který je zobrazen v horní části stránky. K vyhledání interního názvu otevřete stránku, jejíž interní název potřebujete, a kamkoli klikněte pravým tlačítkem na stránce. Po otevření nabídky najeďte myší nad položku **Informace formuláře**. Interní název formuláře se zobrazí vedle položky menu **Informace formuláře**.
 
> - Určete ovládací prvek formuláře, ze kterého aplikace může načíst kontextová data. Aplikace může například použít data týkající se pracovníka. Pokud zadáte stránku **Pracovník** do pole **Kontext**, otevře se stránka **Pracovník** při spuštění aplikace. Zadání do **kontextového pole** není povinné. 
> - Nastavte velikost dialogové okno, ve kterém bude spuštěna aplikace PowerApps. Dialogová okna jsou označena jako malá nebo velká pro optimalizaci uživatelského rozhraní pro spuštění vaší aplikace buď na telefonu nebo na větším zařízení. 

Můžete také určit, pro které právnické osoby bude aplikace dostupná, nebo ji můžete zpřístupnit pro všechny právnické osoby. Standardně jsou aplikace PowerApps k dispozici pro všechny právnické osoby.

## <a name="opening-an-application"></a>Otevření aplikace
Po dokončení konfigurace integrované aplikace PowerApps se přidají odkazy na vámi určené aplikace na stránky v rámci aplikace Talent. Klikněte na odkaz, pokud chcete aplikaci otevřít. 



