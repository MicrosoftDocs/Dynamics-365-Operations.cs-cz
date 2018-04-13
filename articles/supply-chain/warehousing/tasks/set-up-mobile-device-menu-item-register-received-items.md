--- 
title: "Nastavení položky nabídky na mobilním zařízení pro registraci přijatých položek"
description: "Tato úloha je zaměřena na nastavení položky nabídky mobilního zařízení."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7b5d757361c1163bbd0300abd3da4e0a2dd6b0e0
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Nastavení položky nabídky na mobilním zařízení pro registraci přijatých položek

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tato úloha je zaměřena na nastavení položky nabídky mobilního zařízení. Tato položka nabídky slouží k registraci příjmu položek, které jsou objednány prostřednictvím nákupních objednávek. 

Tohoto průvodce můžete použít s ukázkových dat společnosti USMF. Tento postup je určen pro vedoucího skladu.


## <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení
1. Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení.
2. Klikněte na položku Nová.
3. Do pole Položky nabídky mobilního zařízení zadejte hodnotu.
    * Toto je jedinečný identifikátor pro tuto položku nabídky mobilního zařízení. Můžete například zadat „Registrace mé nákupní objednávky“.  
4. Zadejte hodnotu do pole Titul.
    * Toto je název, který se zobrazí uživateli mobilního zařízení. Můžete například zadat „Registrace nákupní objednávky“.  
5. V poli Režim vyberte „Práce“.
    * Registrací množství na skladě obdrženého pro řádek nákupní objednávky bude vytvořena práce pro přesunutí zboží z místa příjmu do zásob. Práce se nevytvoří, dokud jsou položky registrovány.  Proto nechejte hodnotu možnosti Použít stávající práci nastavenou na Ne.  
6. Rozbalte nebo sbalte oddíl Obecné.
7. V poli Proces pro vytvoření práce vyberte „Přijetí položky nákupní objednávky“.
    * Řádek nákupní objednávky musí být identifikován jedinečným způsobem předtím, než ho bude možné registrovat ve skladu. V tomto scénáři mobilní zařízení zaznamená číslo nákupní objednávky a číslo položky, a tím bude umožněno systému identifikovat řádek nákupní objednávky. Pracovní vyskladnění bude vytvořeno a může být vyzvednuto jiným pracovníkem.    Metoda vytvoření práce, kterou jste vybrali, určuje, která pole budou k dispozici na pevné záložce Obecné.  
    * Pokud vyberete možnost Použít výchozí data, tlačítko Výchozí data bude aktivní. Zde můžete zvolit pole k zobrazení dat, která pracovník obvykle potřebuje ve své každodenní práci, takže tyto hodnoty budou zobrazeny na mobilním zařízení.  
    * Parametr seskupení poznávacích značek se používá v kombinaci se skupinou klasifikace jednotek, která je přiřazena k položce, která je přijímána. Můžete upřesnit, zda příjmy menší než nebo větší než jedna paleta by měly být seskupeny do jedné registrační značky nebo rozděleny do více jednotlivých registračních značek pro každou jednotku.  
    * Pokud vyberete možnost Generování poznávací značky, vytvoří se tím na základě výběru číselné řady jedinečné registrační číslo.   
    * Můžete vybrat šablonu, která bude použita, když je vytvořena práce. Pokud například zaregistrujete položku pro nákupní objednávku, práce vyskladnění se vytvoří na základě šablony práce. Pokud zde nevyberete šablonu práce, systém na základě kritérií dotazu přiřadí šablonu, která je asociována se šablonami.  
    * Pokud se dispoziční kódy zobrazí v mobilním zařízení, mohou pracovníci vyhodnocovat stav nebo kvalitu položek a vybírat příslušný kód. Pravidla pro dispoziční kód určují, zda položky budou k dispozici i pro jiné procesy ve skladu. Pravidla rovněž určují, jaké směrnice skladového místa se používají pro práci, která je vytvořena.   
    * Pokud vyberete možnost Kódy dispozice dávky, mohou pracovníci vyhodnocovat stav nebo kvalitu dávky a vybírat příslušný dispoziční kód.  Pravidla, která jsou nastavena pro dispoziční kód dávky určují, zda dávka bude k dispozici i pro jiné procesy ve skladu.  
    * Pokud vyberete možnost tisknout štítky, štítky poznávací značky se vytisknou automaticky při přijetí položky.  
8. Klikněte na položku Uložit.
9. Zavřete stránku.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Přidání položky nabídky do nabídky mobilního zařízení
1. Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení.
2. Použijte rychlý filtr k filtrování v poli Název s hodnotou „vstupní“.
3. Klikněte na možnost Upravit.
4. Ve stromové struktuře vyberte „Ve stromu dostupné nabídky a položek vyberte položku nabídky vytvořenou dříve“.
    * Vyberte položku nabídky, kterou jste vytvořili předtím.  
5. Klepněte na šipku ukazující napravo.
6. Klikněte na položku Uložit.
7. Zavřete stránku.


