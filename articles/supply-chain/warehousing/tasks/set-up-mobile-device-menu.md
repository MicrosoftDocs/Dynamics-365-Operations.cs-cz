---
title: Nastavení položky nabídky v mobilním zařízení pro dokončení práce typu Nákupní objednávka
description: Toto téma ukazuje způsob nastavení položky nabídky Mobilní zařízení.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21994acabd254d0f10c7f22bbc83e4dbd69fad04
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814433"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Nastavení položky nabídky v mobilním zařízení pro dokončení práce typu Nákupní objednávka

[!include [banner](../../includes/banner.md)]

Toto téma ukazuje způsob nastavení položky nabídky Mobilní zařízení. V tomto příkladu slouží tato položka nabídky k provedení práce typu Nákupní objednávka. Platná práce je určena pracovní třídou, která je přiřazena k položce nabídky. Tohoto průvodce můžete použít s ukázkových dat společnosti USMF. Tento proces obvykle provádí správce skladu.


## <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení
1. Přejděte na **Položky nabídky mobilního zařízení** zadáním do vyhledávacího panelu.
2. Zvolte **Nové**.
3. Do pole **Název položky nabídky** zadejte hodnotu. Zadejte jedinečnou hodnotu. Můžete například zadat `POMove`. Zapamatujte si hodnotu – budete ji potřebovat později.  
4. Zadejte hodnotu do pole **Nadpis**. Toto je název, který se zobrazí na mobilním zařízení. Můžete například zadat `PO Move`.  
5. V poli **Režim** vyberte **Práce**.
6. V poli **Použít stávající práci** vyberte možnost **Ano**.
    - Tato položka nabídky v mobilním zařízení se používá k provedení stávající práce. Proto je nutné nastavit tuto hodnotu na hodnotu **Ano**.  
    - Pole **Zobrazit stav zásob určuje**, zda se stav zásob na skladě zobrazí pracovníkovi skladu na mobilním zařízení.  
7. V poli **Řídí** vyberte **Systémové seskupení**. Pokud vyberete jinou možnost v poli **Řídí**, v části **Obecné** na této stránce se zobrazí další pole. Zobrazená pole závisí na vašem výběru. Při výběru možnosti **Systémové seskupení** budou přidána dvě nová pole. Ty jsou vysvětleny níže.  
8. V poli **Systémové seskupení** vyberte **WorkPoolId**. Když pracovníci skladu otevřou tuto položku nabídky, budou vyzváni ke kontrole ID fondu práce. Uživateli budou předloženy všechny pracovní objednávky s tímto ID fondu práce a otevřené řádky pracovního příkazu, do kterých byla k této položce nabídky přidána některá z pracovních tříd.  
9. Zadejte hodnotu do pole **Popisek systémového seskupení**. Tento textový popisek se zobrazí uživateli mobilního zařízení. Můžete například zadat **Fond práce**.  
10. Vyberte možnost **Ano** v poli **Přepsat registrační značku během vložení**. Tato možnost umožňuje pracovníkům skladu přepsat cílové registrační značky, když jsou položky odloženy do umístění řízeného registračními značkami.  
11. Vyberte možnost **Ano** v poli **Odložená skupina**.
    - Pokud všechny řádky vložení v pracovní objednávce sdílí stejné umístění, uživatel obdrží jednu kombinovanou instrukci pro vložení pro všechny řádky. 
    - ID šablony auditu: šablona auditu práce umožňuje určit, zda je třeba pracovní proces pro položku nabídky přerušit, aby mohla být provedena jiná operace. Pokud je tedy například tato položka nabídky určena pro vstupní práci, šablona auditu může vyžadovat, aby pracovník ověřil teplotu. Bod, ve kterém bude proces přerušen, je určen v šabloně auditu, a může se například jednat o zahájení nebo dokončení práce, nebo o okamžik, kdy dojde ke změně stavu.  
12. Rozbalte sekci **Pracovní třídy**.
13. Zvolte **Nové**.
14. Zadejte `Purchase` do pole **ID pracovní třídy**. Pracovní fond omezuje práci, pro kterou lze používat položku nabídky. V tomto případě se použije pro otevřené řádky pracovního příkazu, které mají ID třídy pro práci u nákupu.  
15. Zvolte **Uložit**.

## <a name="set-up-work-confirmation"></a>Potvrzení nastavení práce
1. Vyberte **Nastavení potvrzení práce**.
2. V poli **Typ práce** vyberte **Vybrat**.
3. Zaškrtněte políčko **Potvrdit automaticky**. Pracovní instrukce s typem práce „vyskladnění“ bude automaticky potvrzena. Tento pokyn není prezentován uživateli.  
4. Zvolte **Nové**.
5. V poli **Typ práce** vyberte „Vložit“.
6. Zaškrtněte políčko **Potvrzení umístění**. Pracovník skladu, bude požádán, aby provedl kontrolní skenování v umístění, ve kterém je zboží odloženo.  
7. Zvolte **Uložit**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Přidání položky nabídky do nabídky mobilního zařízení
1. Přejděte do nabídky **Mobilní zařízení** jeho zadáním do vyhledávacího panelu.
2. Vyberte možnost **Upravit**.
3. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli **Jméno** pomocí hodnoty **inbound**. Chcete najít nabídku, kterou lze použít pro vstupní položky nabídky. V USMF se tato položka nazývá **Příchozí**.  
4. Ve stromu vyberte **hodnotu**.
5. Vyberte šipku ukazující napravo.
6. Zvolte **Uložit**.
7. Zavřete stránku.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]