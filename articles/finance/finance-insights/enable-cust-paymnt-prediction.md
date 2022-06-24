---
title: Povolit předpovědi plateb od zákazníka
description: Tento článek vysvětluje, jak zapnout a nakonfigurovat funkci předpovědi plateb zákazníka ve Finančních přehledech.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f04ee9db5efe3595dea30d641c5097d6b90c0d77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898200"
---
# <a name="enable-customer-payment-predictions"></a>Povolit předpovědi plateb od zákazníka

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak zapnout a nakonfigurovat funkci předpovědi plateb zákazníka ve Finančních přehledech. Funkci zapnete v pracovním prostoru **Správa funkcí** a zadejte nastavení konfigurace na stránce **Konfigurace Finance Insights**. Tento článek také obsahuje informace, které vám mohou pomoci tuto funkci efektivně využívat.

> [!NOTE]
> Než dokončíte následující kroky, nezapomeňte provést nezbytné kroky v článku [Konfigurace pro finanční přehledy](configure-for-fin-insites.md).

1. Zapněte funkci Prognózy plateb zákazníků:

    1. Otevřete pracovní prostor **Správa funkcí**.
    2. Vyberte možnost **Zkontrolovat aktualizace**.
    3. Na kartě **Vše** vyhledejte **Prognózy plateb zákazníků**. Pokud tuto funkci nemůžete najít, vyhledejte **(Preview) Prognózy plateb zákazníků**. 
    4. Zapnutí funkce.

    Funkce Prognózy plateb zákazníků je nyní zapnutá a připravená ke konfiguraci.

2. Konfigurujte funkci přehledy plateb zákazníků:

    1. Přejděte na **Kredit a inkasa \> Nastavení \> Finance Insights \> Prognózy plateb zákazníků**.
    2. Na stránce **Konfigurace Finance Insights** na kartě **Prognózy plateb zákazníků** vyberte **Zobrazit datová pole použitá v predikčním modelu** pro otevření stránky **Datová pole pro predikční model**. Zde si můžete prohlédnout výchozí seznam polí, která se používají k vytvoření modelu predikce umělé inteligence (AI) pro předpovědi plateb zákazníků.

        Chcete-li k vytvoření predikčního modelu použít výchozí seznam polí, zavřete stránku **Datová pole pro predikční model** a poté na stránce **Konfigurace Finance Insights** nastavte možnost **Povolit funkci** na **Ano**.
        
   > [!NOTE]
   > Funkce **Předpovědi plateb zákazníků** vyžaduje více než 100 transakcí za předchozích šest až devět měsíců. Transakce mohou zahrnovat volné faktury, prodejní objednávky a platby zákazníků. Tato data musí být rozložena do všech nastavení **Včas**, **Pozdě** a **Velmi pozdě**.    
     

    3. Zadejte období transakce "velmi pozdě" a definujte, co predikční kontejner **Velmi pozdě** znamená pro vaši obchodní činnost.

        U každé otevřené faktury systém předpovídá pravděpodobnost platby ve třech kontejnerech: **Včas**, **Pozdě** a **Velmi pozdě**.

        - **Včas** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny v den splatnosti transakce nebo před ním.
        - **Pozdě** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny po datu splatnosti transakce, ale před začátkem „velmi pozdního“ období transakce.
        - **Velmi pozdě** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny po začátku „velmi pozdního“ období transakce.

        > [!NOTE]
        > Pokud změníte „velmi pozdní“ období transakce a vyberete **Změnit pozdní prhovou hodnotu** po vytvoření predikčního modelu AI pro platby odběratelům, stávající predikční model se odstraní a vytvoří se nový model. Nový predikční model přesune transakce do období „velmi pozdě“ na základě nastavení, která byla zadána k jeho definování.

    4. Poté, co dokončíte definování období transakce „velmi pozdě“, vyberte **Vytvořte predikční model** k vytvoření predikčního modelu. Část **Predikční model** na stránce **Konfigurace Finance Insights** zobrazuje stav predikčního modelu.

        > [!NOTE]
        > Kdykoli během vytváření predikčního modelu můžete vybrat **Obnovit vytváření modelu** a restartovat proces.

    Funkce byla nyní nakonfigurována a je připravena k použití.

Poté, co byla funkce zapnuta a nakonfigurována a model predikce byl vytvořen a funguje, část **Predikční model** stránky **Parametry Finance Insights** ukazuje přesnost modelu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
