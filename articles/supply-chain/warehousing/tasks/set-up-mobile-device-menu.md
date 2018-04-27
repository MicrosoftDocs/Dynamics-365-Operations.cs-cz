--- 
title: "Nastavení položky nabídky na mobilním zařízení pro dokončení práce v nákupní objednávce"
description: "Tento postup popisuje způsob nastavení položky nabídky Mobilní zařízení."
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b80c258d6a779a8fc5bb6c846abd3af7e69d5e06
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a>Nastavení položky nabídky na mobilním zařízení pro dokončení práce v nákupní objednávce

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob nastavení položky nabídky Mobilní zařízení. V tomto příkladu slouží tato položka nabídky k provedení práce typu Nákupní objednávka. Platná práce je určena pracovní třídou, která je přiřazena k položce nabídky. Tohoto průvodce můžete použít s ukázkových dat společnosti USMF. Tento proces obvykle provádí správce skladu.


## <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení
1. Přejděte do položek nabídky mobilního zařízení.
2. Klikněte na položku Nová.
3. Do pole Položky nabídky mobilního zařízení zadejte hodnotu.
    * Zadejte jedinečnou hodnotu. Můžete například zadat „Přesun nákupní objednávky“. Zapamatujte si hodnotu – budete ji potřebovat později.  
4. Zadejte hodnotu do pole Titul.
    * Toto je název, který se zobrazí na mobilním zařízení. Můžete například zadat „Přesun nákupní objednávky“.  
5. V poli Režim vyberte „Práce“.
6. Vyberte možnost Ano v poli Použít stávající práci.
    * Tato položka nabídky v mobilním zařízení se používá k provedení stávající práce. Proto je nutné nastavit tuto hodnotu na hodnotu Ano.  
    * Pole Zobrazit stav zásob určuje, zda se stav zásob na skladě zobrazí pracovníkovi skladu na mobilním zařízení.  
7. V poli „Řídí“ vyberte „Systémovém seskupení“.
    * Pokud vyberete jinou možnost v poli Řídí, v části Obecné na této stránce se zobrazí další pole. Zobrazená pole závisí na vašem výběru. Při výběru možnosti Systémové seskupení budou přidána dvě nová pole. Ty jsou vysvětleny níže.  
8. V poli Systémové seskupení vyberte WorkPoolId.
    * Když pracovníci skladu otevřou tuto položku nabídky, budou vyzváni ke kontrole ID fondu práce. Uživateli budou předloženy všechny pracovní objednávky s tímto ID fondu práce a otevřené řádky pracovního příkazu, do kterých byla k této položce nabídky přidána některá z pracovních tříd.  
9. Zadejte hodnotu do pole Popisek systémového seskupení.
    * Tento textový popisek se zobrazí uživateli mobilního zařízení. Můžete například zadat „Fond práce“.  
10. Vyberte možnost Ano v poli Přepsat registrační značku během vložení.
    * Tato možnost umožňuje pracovníkům skladu přepsat cílové registrační značky, když jsou položky odloženy do umístění řízeného registračními značkami.  
11. Vyberte možnost Ano v poli Odložená skupina.
    * Pokud všechny řádky vložení v pracovní objednávce sdílí stejné umístění, uživatel obdrží jednu kombinovanou instrukci pro vložení pro všechny řádky.  
    * ID šablony auditu: šablona auditu práce umožňuje určit, zda je třeba pracovní proces pro položku nabídky přerušit, aby mohla být provedena jiná operace. Pokud je tedy například tato položka nabídky určena pro vstupní práci, šablona auditu může vyžadovat, aby pracovník ověřil teplotu. Bod, ve kterém bude proces přerušen, je určen v šabloně auditu, a může se například jednat o zahájení nebo dokončení práce, nebo o okamžik, kdy dojde ke změně stavu.  
12. Rozbalte sekci Pracovní třídy.
13. Klikněte na položku Nová.
14. Zadejte „Nákup“ do pole ID pracovní třídy.
    * Pracovní fond omezuje práci, pro kterou lze používat položku nabídky. V tomto případě se použije pro otevřené řádky pracovního příkazu, které mají ID třídy pro práci u nákupu.  
15. Klikněte na položku Uložit.

## <a name="set-up-work-confirmation"></a>Potvrzení nastavení práce
1. Klepněte na Nastavení potvrzení práce.
2. V poli Typ práce vyberte „Vybrat“.
3. Zaškrtněte políčko Potvrdit automaticky.
    * Pracovní instrukce s typem práce „vyskladnění“ bude automaticky potvrzena. Tento pokyn není prezentován uživateli.  
4. Klikněte na položku Nová.
5. V poli Typ práce vyberte „Vložit“.
6. Zaškrtněte políčko Potvrzení umístění.
    * Pracovník skladu, bude požádán, aby provedl kontrolní skenování v umístění, ve kterém je zboží odloženo.  
7. Klikněte na položku Uložit.
8. Zavřete stránku.
9. Zavřete stránku.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Přidání položky nabídky do nabídky mobilního zařízení
1. Přejděte do nabídky Mobilní zařízení.
2. Klikněte na položku Upravit.
3. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „inbound“.
    * Chcete najít nabídku, kterou lze použít pro vstupní položky nabídky. V USMF se tato položka nazývá Příchozí.  
4. Ve stromu vyberte „hodnotu“.
5. Klepněte na šipku ukazující napravo.
6. Klikněte na položku Uložit.
7. Zavřete stránku.


