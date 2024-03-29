---
title: Zadání počátečních zůstatků mezd
description: Tento článek popisuje postup při zadávání počátečních zůstatků pro kódy příjmů, srážky, odměny a daně.
author: twheeloc
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21cd8b3f68627a8255df82ee818e919b3ac20f88
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167792"
---
# <a name="enter-payroll-beginning-balances"></a>Zadání počátečních zůstatků mezd

[!include [banner](../../includes/banner.md)]

Tento článek popisuje postup při zadávání počátečních zůstatků pro kódy příjmů, srážky, odměny a daně. Tyto informace jsou důležité pro partnery, kteří přenášejí data pro novou implementaci mezd z jiného systému. V rámci přípravy na zadání počátečních zůstatků mezd ověřujeme následující údaje:

- Záznamy zaměstnance jsou zadané a dostupné v systému.
- Následující údaje jsou nastaveny a přiřazeny zaměstnancům:

    - Platební cykly a platební období
    - Kódy příjmů
    - Daně
    - Výhody a srážky

- Společnost by měla zvolit datum, kdy lze nastavit počáteční zůstatky mezd.
- Informace byla získána na základě všech výdělků, zaměstnaneckých výhod / odpočtů, příspěvků na zaměstnanecké výhody, daní zaměstnanců a daních zaměstnavatelů a jejich částek od začátku roku ze zastaralého systému.

Při plánování zadávání počátečních zůstatků zvažte, jak podrobná mají data být. Většina firem zadává jednu konsolidovanou částku od začátku roku. Pokud jsou však potřeba podrobnější informace, lze zůstatky zadávat v přírůstcích po čtyřech. Rozhodování o tom, jaká úroveň podrobností je potřeba, určuje, kolik ručních výkazů mezd musí být vytvořeno pro každého zaměstnance. U jednotlivé částky od začátku roku je potřeba pouze jeden ruční výkaz pro každého zaměstnance. K tomu použijte dosud realizované částky z výpisu konečné platby z předchozího systému jako částku zadanou do nového mzdového systému.

Následující příklad ukazuje, jak zadat počáteční zůstatky mezd zaměstnance, včetně kódů příjmů, odměn odpočitatelných položek a daně. V praxi byste měli položku řádku pro každý kód příjmů, odpočtu na zaměstnanecké výhody, příspěvku na zaměstnaneckou výhodu, daně pro zaměstnance a zaměstnavatele s dosud zadanou částkou od začátku roku. Pomocí tohoto seznamu kódů a částek postupujte podle pokynů pro vytvoření ručního výkazu příjmů a plateb s vypnutým účetnictvím pro přenesení počátečních zůstatků za účelem výpočtu mezd. Vzhledem k tomu, že nebudete chtít tento výkaz počátečního zůstatku zaúčtovat do hlavní knihy, zakážete účetnictví. Tak to probíhalo v zastaralém systému a bylo přeneseno do nového systému při nastavování počátečních zůstatků v hlavní knize.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Jak nastavit kódy příjmů pro použití v mzdovém systému počátečních zůstatků

Pokud zadáváte počáteční zůstatky mezd, ujistěte se, že kódy příjmů, které budete používat, jsou nakonfigurovány s povolenou možností "Úpravy příjmů výkazu sazby". To vám umožní zadat ručně částku ze systému ze starší verze. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Vytvoření výkazu příjmů pro zaměstnance tak, aby obsahoval počáteční zůstatek

Tento krok ručně vytvoří mzdový výkaz pro každého zaměstnance za poslední platební období v systému ze starší verze, což vytvoří řádky výkazu příjmů v novém mzdového systému. Zadejte jeden řádek pro na kód příjmu a částku a hodiny od začátku roku. Ukázkové kroky:

1. Otevřete stránku **Výkazy všech příjmů** a klepněte na tlačítko **Nový**.

    Zadejte následující: 

    | Pole      | Hodnota                 |
    |------------|-----------------------|
    | Pracovní podproces     | Michael Redmond       |
    | Platební cyklus  | sm                    |
    | Mzdové období | 6/16/2017 - 6/30/2017 |

2. Na kartě **Řádek výkazu příjmů** zadejte následující:

    Řádek 1: karta **Řádek výkazu příjmů**

    | Pole            | Hodnota       |
    |------------------|-------------|
    | Kód příjmů    | Standardní mzda |
    | Množství         | 1.00        |
    | Kurz             | 30,000      |
    | Karta Detaily řádku |             |
    | Ruční           | (označeno)    |

    Řádek 2: karta **Řádek výkazu příjmů**

    | Pole            | Hodnota    |
    |------------------|----------|
    | Kód příjmů    | Prémie    |
    | Množství         | 1.0000   |
    | Kurz             | 4250.00  |
    | Karta Detaily řádku |          |
    | Ruční           | (označeno) |

    Řádek 3: karta **Řádek výkazu příjmů**

    | Pole           | Hodnota      |
    |-----------------|------------|
    | Kód příjmů   | Komise |
    | Množství        | 1.0000     |
    | Kurz            | !,299.00   |
    | Kurz            | 1,299.00   |
    | Karta Detaily řádku |            |
    | Ruční          | (označeno)   |

    > [!NOTE]
    > Nastavení posuvníku **Ruční** na hodnotu **Ano** v poli **Podrobnosti řádku** pro každý řádek výkazu příjmů je klíčem pro počáteční zůstatky mezd zadané pro každého zaměstnance.

3. V podokně **akce** klepněte na tlačítko **Uvolnění výkazu příjmů** USA FED ER FICA.
4. V podokně **akce** klepněte na **Platební příkaz** pro otevření stránky **Generovat platební výkazy** stránky a nastavte následující:

    | Pole              | Hodnota     |
    |--------------------|-----------|
    | Datum platby       | 30. 6. 2017 |
    | Typ cyklu plateb   | Ruční    |
    | Zakázat účetnictví |   Ano     |

    > [!NOTE] 
    > To je dostupné pouze, když je typ spuštění platby ručně a uživatel chce zakázat účtování ve spuštění platů.

    Klikněte na tlačítko **OK** a zavřete **Infolog**.

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a>Proč musí být při generování výkazů mezd posuvník na hodnotě Zakázat účtování nastavený na Ano?

Nastavením posuvníku na hodnotu **Ano** se zabrání distribuci řádků ve výkazu mezd a jejich rozúčtování do hlavní knihy. Pokud byly zadány účetní zůstatky ze systému ze staršího systému, byly částky v hlavní knize aktualizovány dříve. Zadání počátečních zůstatků pro zpracování mezd umožňuje generovat sestavy, které budou zahrnovat informace z předchozích let a identifikovat limity pro účely zaměstnaneckých výhod a daní.

### <a name="c-create-pay-statements-for-employees"></a>C. Vytvoření výkazů plateb pro zaměstnance

Po generování výkazů mezd, které mají počáteční zůstatky, je nutné ověřit, že výkazy mezd přesně odpovídají mzdovým datům. Je také nutné ručně aktualizovat informace o zaměstnaneckých výhodách a daních tak, aby odpovídaly hodnotám v předchozím mzdovém systému. Po ověření, že částky z předchozího systému mezd odpovídají částkám v aktuálním výkazu mezd, musíte dokončit výkazy mezd.

1. Otevřete stránku **všechny platební příkazy**.
2. Zvýraznění posledního generovaného mzdového výpisu pro Michaela Redmonda
3. Kliknutím na tlačítko **upravit** otevřete stránku **mzdový výkaz**.
4. Otevřete kartu **Odpočty zaměstnaneckých výhod** a zadejte následující:

    | Pole             | Hodnota            |
    |-------------------|------------------|
    | Zam. výhoda           | Částka odpočtu |
    | 401K              | Účast      |
    | Zubní            | SubSp            |
    | Útrata za péči | Účast      |
    | Vize            | SupSp            |

5. Na kartě **Odpočty zaměstnaneckých výhod** zadejte následující:

    | Pole   | Hodnota               |
    |---------|---------------------|
    | Zam. výhoda | Částka příspěvku |
    | 401K    | Účast         |
    | Zubní  | SubSp               |
    | Vize  | SubSp               |

6. Na kartě **Daňové odpočty** zadejte následující:

    | Pole           | Hodnota            |
    |-----------------|------------------|
    | Kód daně        | Částka odpočtu |
    | USA FED ER FICA | 1600.00          |
    | USA FED ER MEDI | 825.75           |

7. Na kartě **Daňové příspěvky** zadejte následující:
8. Klikněte na tlačítko **Vypočítat.**

    > [!IMPORTANT] 
    > Ověřte celkové částky výkazu mezd, aby odpovídaly hodnotě od počátku roku systému ze starší verze pracovníka. Můžete chtít zablokovat dokončení v dalším kroku, abyste mohli provést komplexní ověřování všech výkazů mezd celkem. Po ověření spusťte všechny výkazy mezd a dokončete je.

Stejný postup lze provést v přírůstcích po čtvrtletí, pokud je to potřeba u všech předchozích kvartálů v každém období. To je potřeba, pouze pokud zákazník musí zobrazit data podle čtvrtletí bez návratu zpět do systému ze starší verze.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Pokud uděláte chybu při zadávání počátečních zůstatků pro zaměstnance

Je možné stornovat a znovu zadávat transakce. Chcete-li transakci stornovat, vše, co je nutné provést, je provést následující kroky na stránce **všechny platební příkazy**.

1. Klepněte na tlačítko **stornovat**.
2. Klepněte na tlačítko **Ano** po zobrazení zprávy "Při stornování tohoto výkazu mezd se vytvoří storno platby pro vyrovnání v tomto výkazu mezd. Nelze upravit žádný výkaz mezd. Chcete stornovat tento výkaz mezd?" . 

Po stornování výkazu mezd můžete generovat nový výkaz mezd pracovníka na základě předtím vytvořeného výkazu mezd. Je nutné opravit jakékoli nesprávné řádky ve výkazu zisků předtím, než budete generovat nový výkaz mezd, a následně generovat nové výkazy mezd se správnými částkami. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
