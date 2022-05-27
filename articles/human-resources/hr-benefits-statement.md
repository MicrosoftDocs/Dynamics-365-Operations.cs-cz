---
title: Výkaz zaměstnaneckých výhod
description: Sestava výkazu výhod vysvětluje výhody, které má zaměstnanec aktuálně registrovány.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a12649cd0604fb6acd58420fdafb5b560fcc10cf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688225"
---
# <a name="benefit-statement"></a>Výkaz zaměstnaneckých výhod


[!INCLUDE [PEAP](../includes/peap-2.md)]

Sestava **Výkaz výhod** poskytuje výpis výhod, které má zaměstnanec aktuálně registrovány. K sestavě má přístup přímo zaměstnanec nebo správce výhod. **Výkaz výhod** poskytuje seznam zaregistrovaných zaměstnaneckých výhod, možností disponibility, nákladů a všech registrovaných závislých osob nebo příjemců výhod. Výkaz lze vytisknout pro jednoho pracovníka nebo pro více pracovníků.

> [!NOTE]
V pracovním prostoru **Správa funkcí** musí být zapnutá funkce **Výkaz výhod**. Aby to bylo možné provést, funkci **Správa výhod** je nutné zapnout ve správě funkcí. 


## <a name="importing-the-benefit-statement"></a>Import výkazu výhod 

**Výkaz výhod** musíte importovat pomocí konfigurace sestavy předtím, než bude **Výkaz výhod** k dispozici. To lze provést následovně:

1.  Přejděte do pracovního prostoru **Správa systému**.

2.  Vyberte dlaždici **Elektronické výkaznictví**.

3.  Přejděte do **Poskytovatelů konfigurace** a vyberte **Úložiště**.

  ![Výběr položky Úložiště.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  V seznamu vyberte položku **HR zdroje** a poté vyberte **Otevřít**.

    ![Úložiště konfigurací.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  V levém podokně vyberte **Model výkazu výhod** a rozbalte jej tak, aby se zobrazil **Formát výkazu výhod**.

6.  V levém podokně vyberte **Formát výkazu výhod**.

7.  Na pravé straně obrazovky bude záložka **Verze**. Vyberte **Import**.

    ![Záložka Verze.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Generování výkazu výhod jako souboru PDF

Standardně je **Výkaz výhod** tištěn jako dokument aplikace Microsoft Word. Chcete-li ho tisknout ve formátu PDF, budete muset konfigurovat možnost PDF v **Místu určení elektronického výkaznictví**. 

1. Chcete-li to provést, přejděte na **Pracovní prostor pro správu systému** > **Elektronické výkaznictví** > **Související odkazy** > **Místo určení elektronického výkaznictví**.

1.  Zvolte **Nové**.

2.  V poli **Reference** vyberte **Formát výkazu výhod**.

3.  Na záložce **Místo určení souboru** vyberte **Nové**.

4.  Do pole **Název** zadejte **Výkaz výhod (PDF)**.

5.  V poli **Název součásti souboru** vyberte **Výkaz výhod**.

6.  Vyberte zaškrtávací políčko **Převést na PDF**.

7.  V položce nabídky vyberte **Nastavení**. 

    ![Místo určení souboru.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Vyberte záložku **Soubor** a poté vyberte **Povoleno**.

9.  Vyberte **OK**.
   
> [!NOTE]
> Funkce správy zaměstnaneckých výhod je ve stavu Preview. Při používání nastavení e-mailového místa určení v sestavě **Místo určení elektronického výkaznictví** narazíte na známý problém. Může se zobrazit chybová zpráva a e-mail se nepodaří odeslat.

**Výkaz výhod** lze generovat z následujících stránek:

-   **Pracovní prostor správy zaměstnaneckých výhod** > **Odkazy** > **Sestavy** > **Výkaz výhod**

-   **Zaměstnanci (starší formulář)** > **karta Osobní údaje** > **Výkaz výhod**

-   **Zjednodušené zadávání zaměstnance** > **Výkazy výhod** > **Výkaz výhod**

-   **Samoobsluha zaměstnanců** > **Výhody** > **Zobrazit výkaz výhod**

> [!NOTE]
>  Přístup k **Výkazu výhod** v **Samoobsluze zaměstnanců** je řízen oprávněním **Zobrazit výkaz výhod**. To se nachází pod povinností **Samoobslužné výhody pro zaměstnance**. Toto oprávnění je zaměstnancům standardně uděleno.

## <a name="report-contents"></a>Obsah sestavy

**Výkaz výhod** vytiskne potvrzené výběry plánu zaměstnance, včetně všech plánů, kterých se vzdal. Na následujícím obrázku je znázorněn příklad této sestavy. 

![Sestava výkazu výhod.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Sestava zobrazí **Plán**, **Možnost disponibility**, **Náklady na zaměstnance** a **Náklady zaměstnavatele**. Sestava také vyjmenuje všechny pokryté závislé osoby. Pokud jsou k plánu přidružení příjemci výhod, zobrazí se příjemci a jejich priorita distribuce a procenta.

Sestavu **Výkaz výhod** lze vytisknout pro více zaměstnanců současně s využitím záložky **Záznamy k zahrnutí** na stránce **Výkaz výhod**.
