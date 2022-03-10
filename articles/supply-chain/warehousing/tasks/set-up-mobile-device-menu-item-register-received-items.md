---
title: Nastavení položky nabídky na mobilním zařízení pro registraci přijatých položek
description: Toto téma je zaměřeno na nastavení položky nabídky mobilního zařízení.
author: Mirzaab
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 410a70294e5a417950ed5332ec5fdd7da321a31d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565152"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Nastavení položky nabídky na mobilním zařízení pro registraci přijatých položek

[!include [banner](../../includes/banner.md)]

Toto téma je zaměřeno na nastavení položky nabídky mobilního zařízení. Tato položka nabídky slouží k registraci příjmu položek, které jsou objednány prostřednictvím nákupních objednávek. 

Tohoto průvodce můžete použít s ukázkových dat společnosti USMF. Tento postup je určen pro vedoucího skladu.


## <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení
1. V navigačním podokně přejděte do nabídky **Moduly > Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení**.
2. Zvolte **Nové**.
3. Do pole **Název položky nabídky** zadejte hodnotu. Toto je jedinečný identifikátor pro tuto položku nabídky mobilního zařízení. Můžete například zadat `My PO registration`.  
4. Zadejte hodnotu do pole **Nadpis**. Toto je název, který se zobrazí uživateli mobilního zařízení. Můžete například zadat `PO registration`.  
5. V poli **Režim** vyberte **Práce**. Registrací množství na skladě obdrženého pro řádek nákupní objednávky bude vytvořena práce pro přesunutí zboží z místa příjmu do zásob. Práce se nevytvoří, dokud jsou položky registrovány. Proto nechejte hodnotu možnosti **Použít stávající práci** nastavenou na **Ne**.
6. V poli **Proces pro vytvoření práce** v sekci **Obecné** vyberte **Přijetí položky nákupní objednávky**.
    - Řádek nákupní objednávky musí být identifikován jedinečným způsobem předtím, než ho bude možné registrovat ve skladu. V tomto scénáři mobilní zařízení zaznamená číslo nákupní objednávky a číslo položky, a tím bude umožněno systému identifikovat řádek nákupní objednávky. Pracovní vyskladnění bude vytvořeno a může být vyzvednuto jiným pracovníkem. Metoda vytvoření práce, kterou jste vybrali, určuje, která pole budou k dispozici na pevné záložce **Obecné**.  
    - Pokud vyberete možnost **Použít výchozí data**, tlačítko **Výchozí data** bude aktivní. Zde můžete zvolit pole k zobrazení dat, která pracovník obvykle potřebuje ve své každodenní práci, takže tyto hodnoty budou zobrazeny na mobilním zařízení.  
    - Parametr **Seskupení poznávacích značek** se používá v kombinaci se skupinou klasifikace jednotek, která je přiřazena k položce, která je přijímána. Můžete upřesnit, zda příjmy menší než nebo větší než jedna paleta by měly být seskupeny do jedné registrační značky nebo rozděleny do více jednotlivých registračních značek pro každou jednotku.  
    - Pokud vyberete možnost **Generování poznávací značky**, vytvoří se tím na základě výběru číselné řady jedinečné registrační číslo.  
    - Můžete vybrat šablonu, která bude použita, když je vytvořena práce. Pokud například zaregistrujete položku pro nákupní objednávku, práce vyskladnění se vytvoří na základě šablony práce. Pokud zde nevyberete šablonu práce, systém na základě kritérií dotazu přiřadí šablonu, která je asociována se šablonami.  
    - Pokud se dispoziční kódy zobrazí v mobilním zařízení, mohou pracovníci vyhodnocovat stav nebo kvalitu položek a vybírat příslušný kód. Pravidla pro dispoziční kód určují, zda položky budou k dispozici i pro jiné procesy ve skladu. Pravidla rovněž určují, jaké směrnice skladového místa se používají pro práci, která je vytvořena.   
    - Pokud vyberete možnost **Kódy dispozice dávky**, mohou pracovníci vyhodnocovat stav nebo kvalitu dávky a vybírat příslušný dispoziční kód. Pravidla, která jsou nastavena pro dispoziční kód dávky určují, zda dávka bude k dispozici i pro jiné procesy ve skladu.  
    - Pokud vyberete možnost **Tisknout štítky**, štítky poznávací značky se vytisknou automaticky při přijetí položky.  
7. Zvolte **Uložit**.
8. Zavřete stránku.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Přidání položky nabídky do nabídky mobilního zařízení
1. V navigačním podokně přejděte do nabídky **Moduly > Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení**.
2. Použijte **Rychlý filtr** k filtrování v poli **Název** s hodnotou `inbound`.
3. Vyberte možnost **Upravit**.
4. Ve dostupných nabídkách a stromu položek vyberte položku nabídky vytvořenou dříve.
5. Vyberte šipku ukazující napravo.
6. Zvolte **Uložit**.
7. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]