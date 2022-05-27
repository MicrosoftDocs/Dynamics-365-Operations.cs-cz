---
title: Vytváření odkazů z aplikace Human Resources do jiného prostředí
description: Toto téma vysvětluje, jak vytvořit odkaz z aplikace Microsoft Dynamics 365 Human Resources do jiného prostředí Dynamics 365.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d20eef4b4861d85ead1d47ca493c3a5c2d2d85e8
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712621"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Vytváření odkazů z aplikace Human Resources do jiného prostředí Finance

Zákazník může mít dvě prostředí Dynamics 365, ve kterých pracuje. Zákazník může mít například prostředí Dynamics 365 Human Resources na finanční infrastruktuře a potřebuje se připojit k jinému prostředí Dynamics 365 Finance. 

Tato funkce povolí odkazy ze stránky Lidské zdroje na konkrétní stránku v jiném prostředí Finance. Když jsou odkazy konfigurovány, můžete určit, kde bude odkaz v Human Resources dostupný, a cílovou stránku, která se otevře v jiném prostředí.

> [!Note] 
> Chcete-li tuto funkci získat, musíte ve **Správě funkcí** zapnout **Vylepšení uživatelského rozhraní Human Resources**.

## <a name="configure-target-systems"></a>Konfigurace cílových systémů

V Human Resources mohou správci systému definovat odkazy, které se zobrazí na stránkách **Human Resources**. Součástmi konfigurace jsou prostředí Finance, do kterých chcete přejít jako do cíle odkazu. 

Postup konfigurace cílového systému:
1. Na stránce **Konfigurovat odkazy** vyberte **Konfigurovat cílový systém**.  
2. Zadejte název cílového systému a zadejte adresu URL prostředí Finance. Po nakonfigurování cílových systémů můžete nadefinovat své odkazy.

## <a name="configure-links"></a>Konfigurovat odkaz

Každý vytvořený odkaz má definovány následující informace:
 - **Odkaz**: Název odkazu. Slouží pouze k identifikaci.
 - **Povolit tento odkaz**: Nastavte tuto možnost na **Ano**, pokud chcete zobrazit odkaz uživatelům aplikace Human Resources.
 - **Zobrazovaný název**: Zapište název, který se zobrazí jako odkaz do druhého prostředí. 
 - **Odkaz na místo zobrazení ve formuláři**: Vyberte, na které stránce se má odkaz zobrazit. Odkazy lze zobrazit pouze v pracovním prostoru **Samoobsluha pro zaměstnance** a na stránkách **Práce**, **Pozice**, **Pracovní formulář**, a **Zjednodušený pracovní formulář**.
 - **Skupina**: Své odkazy můžete uspořádat pomocí skupin. Vyberte existující skupinu nebo vytvořte novou pomocí sloupce **Skupina**.
 - **Cílový systém**: Vyberte cílový systém, který byl vytvořen pomocí možnosti **Konfigurovat cílový systém**. Bude se jednat o sekundární prostředí, které bude použito při navigaci pomocí odkazu.
 - **Použít aktuální společnost uživatele**: Vyberte **Ano**, budete-li chtít používat aktuální společnost uživatele při navigaci do Finance. Pokud zvolíte **Ne**, můžete vybrat společnost, která má být použita.
 - Položka nabídky **Cíl**: Zadejte položku nabídky z prostředí Finance, kterou má používat odkaz při navigaci. K dispozici jsou položky nabídky, ke kterým můžete přímo navigovat. 

   Chcete-li najít požadovanou položku nabídky:
   1. Přejděte do prostředí Finance a otevřete stránku, která je cílem navigace. 
   2. Zkopírujte položku nabídky z adresy URL. Například pokud chcete, aby vás odkaz navedl na seznam zaměstnanců v aplikaci Finance and Operations, zadejte hodnotu, které se objeví v URL adrese za „&mi“. 
   3. Položka nabídky pro navigaci na stránku se seznamem zaměstnanců v tomto příkladu je: HcmWorkerListPage_Employees.

 - **Odkaz na zdroj dat**: Vyberte zdroj dat, na který odkaz ukazuje. Nejběžnější zdroje, jako je například **Pracovník** a **Pozice**, jsou k dispozici.

### <a name="access-to-links"></a>Přístup k odkazům

Správci systému uvidí nově vytvořené odkazy na definovaných stránkách, i když je možnost **Povolit tento odkaz** nastavena na **Ne**. To lze použít k testování odkazů předtím, než budou vystaveny k použití pro jiné zaměstnance. Všechny ostatní role uvidí pouze konfigurované odkazy poté, co bude možnost **Povolit teto odkaz** nastavena na **Ano**. Zaměstnanci, kteří mají přístup ke stránkám, na kterých jsou odkazy k dispozici, budou mít přístup k odkazům.

Uživatelé musí mít v sekundárním prostředí také bezpečnostní práva definovaná pro přístup ke stránkám v tomto prostředí. Pokud ne, zobrazí se při použití odkazu dialogové okno zabezpečení.

