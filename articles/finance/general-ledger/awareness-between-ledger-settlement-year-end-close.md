---
title: Sledování mezi vypořádáním hlavní knihy a uzávěrkou na konci roku
description: Toto téma poskytuje informace o vylepšeních, která mají vliv na vypořádání hlavní knihy a na uzavření hlavní knihy na konci roku.
author: kweekley
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 13d0a0a11a8f31e4ba647ccc23906f6b137051c2
ms.sourcegitcommit: b96e0c70553bca9b3f5eb65105a52cb71d978a36
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/07/2022
ms.locfileid: "8553325"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Sledování mezi vypořádáním hlavní knihy a uzávěrkou na konci roku

[!include [banner](../includes/banner.md)]


V Microsoft Dynamics 365 Finance verze 10.0.25 je funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku** k dispozici v pracovním prostoru **Správa funkcí**. Tato funkce přidává dvě primární vylepšení, která ovlivňují vypořádání hlavní knihy a uzávěrku hlavní knihy na konci roku.

Během roční uzávěrky hlavní knihy již nebudou vypořádané transakce hlavní knihy zahrnuty do počátečního zůstatku příštího fiskálního roku. Toto vylepšení zajišťuje, že do počátečního zůstatku budou zahrnuty pouze nevypořádané transakce hlavní knihy. To je důležité, když se provádí přecenění cizí měny hlavní knihy. Přecenění cizí měny se spouští pouze u transakcí hlavní knihy, které mají stav **Nevyřízeno**. Před zavedením funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku** však počáteční zůstatek shrnoval jak transakce, které mají stav **Vypořádáno**, tak ty, které mají stav **Nevyřízeno** a stav souhrnné částky byl nastaven na **Nevyřízeno**.

Druhé vylepšení umožňuje zaúčtovat podrobné transakce počátečního zůstatku během roční uzávěrky hlavní knihy. Pokud je možnost **Uchovávat podrobnosti na konci roku** je nastavena na **Ano**, bude vytvořen samostatný počáteční zůstatek pro každou transakci hlavní knihy, která není vypořádána. Toto nastavení je definováno pro každý hlavní účet v nastavení vypořádání hlavní knihy. Uchováváním podrobných transakcí pro počáteční zůstatek výrazně zlepšujete schopnost vypořádat nevypořádané transakce hlavní knihy v příštím fiskálním roce.

Na podporu nových vylepšení byly provedeny změny ve vyúčtování účetní knihy a uzávěrce roku.

### <a name="changes-to-ledger-settlement"></a>Změny vypořádání hlavní knihy

- Vypořádání hlavní knihy musí být provedeno během fiskálního roku.
- Vypořádání hlavní knihy musí být provedeno pro transakce na jediném hlavním účtu. Hlavní účet je nyní povinným filtrem na stránce **Vypořádání hlavní knihy**.
- Vypořádání hlavní knihy a zrušení vypořádání hlavní knihy nelze provést u transakcí, které jsou zaúčtovány v rámci uzavřeného fiskálního roku (jinými slovy, uzávěrka na konci roku byla spuštěna).

### <a name="changes-to-year-end-close"></a>Změny ke konci roku

- Uzávěrku na konci roku nelze zrušit, pokud byly v příštím fiskálním roce vypořádány jakékoli transakce počátečního zůstatku. Tato změna se použije, když je zrušena uzávěrka na konci roku nebo když je uzávěrka na konci roku opakována a možnost **Při opětovném uzavírání roku odstranit existující záznamy na konci roku** je nastavena na **Ano** v parametrech hlavní knihy.
- Pokud je možnost **Uchovávat podrobnosti na konci roku** nastavena na **Ano** pro jakýkoli rozvahový účet ve zúčtování hlavní knihy, budou vytvořeny podrobnější transakce počátečního zůstatku pro tento hlavní účet.

## <a name="before-you-enable-the-feature"></a>Než funkci aktivujete

Kvůli změnám ve funkčnosti a datovém modelu je důležité, abyste před aktivací funkce zvážili následující body:

- Protože do počátečního zůstatku jsou převedeny pouze vypořádané transakce, musíte zrušit vypořádání transakcí z aktuálního fiskálního roku, které jsou vypořádány s transakcemi v předchozím fiskálním roce. Transakce musí být vypořádány proti transakcím v rámci aktuálního fiskálního roku. To lze provést prostřednictvím opravné položky v aktuálním fiskálním roce. Úprava ruší souhrnné počáteční zůstatky a kompenzace s podrobnou transakcí nutnou k vypořádání položek hlavní knihy v běžném roce. 

  > [!IMPORTANT]
  > Pokud tak neučiníte, obdržíte chybu **nevyrovnáno** při spuštění uzávěrky na konci roku pro aktuální fiskální rok. Pokud není možné zrušit a znovu vypořádat transakce hlavní knihy se stejným fiskálním rokem, povolte tuto funkci až po dokončení uzávěrky na konci roku. Aktivujte funkci ihned po dokončení uzávěrky na konci roku a před vypořádáním jakýchkoli nových transakcí hlavní knihy v příštím fiskálním roce. 
  
- Všechny transakce, které byly označeny k vypořádání, ale nebyly vypořádány, budou automaticky zrušeny, když je tato funkce povolena. Abyste předešli ztrátě práce, vyrovnejte všechny označené transakce, než funkci povolíte.
- Některé organizace provádějí uzávěrku na konci roku vícekrát za stejný fiskální rok. Funkci nepovolujte, pokud uzávěrka na konci roku již jednou proběhla a bude spuštěna znovu pro stejný fiskální rok. Tato funkce musí být povolena před zpracováním první uzávěrky na konci roku nebo po zpracování poslední uzávěrky na konci roku pro fiskální rok.

  Pokud chcete funkci aktivovat, ale uzávěrka na konci roku již jednou proběhla, musíte před aktivací funkce vrátit uzávěrku na konci roku.

- Protože vypořádání mezi hlavními účty již není povoleno, upravte svou účtovou osnovu nebo procesy podle potřeby, abyste zajistili, že vypořádání hlavní knihy bude možné provést na stejném hlavním účtu.
- Tuto funkci nelze aktivovat, pokud se používá proces uzavření veřejného sektoru na konci roku.

## <a name="set-up-ledger-settlement"></a>Nastavení vypořádání hlavní knihy

Po aktivaci funkce a před spuštěním další uzávěrky na konci roku musí každá organizace určit, zda bude uchovávat podrobnosti o transakci během uzávěrky roku. Volba nemá žádný vliv na zaúčtování počátečního zůstatku z předchozích procesů uzávěrky na konci roku.

Možnost **Uchovávat podrobnosti na konci roku** je nastavena pro každý hlavní účet na stránce **Nastavení vypořádání účetní knihy**.

1.  Přejděte do nabídky **Hlavní kniha** > **Nastavení hlavní knihy** > **Parametry hlavní knihy**.
2.  Na kartě **Vypořádání hlavní knihy** vyberte **Účty vypořádání hlavní knihy**.

- nebo -

1.  Přejděte do nabídky **Hlavní kniha** > **Periodické úkoly** > **Vyrovnání hlavní knihy**.
2.  Vyberte **Účty vypořádání hlavní knihy**.

Na stránku **Vypořádání hlavní knihy** byly přidány dva sloupce:
    
- **Hlavní typ účtu** – Tento sloupec slouží pouze pro informační účely. Zobrazuje typ, který je přiřazen k hlavnímu účtu.
- **Uchovávat podrobnosti na konci roku** – Ve výchozím nastavení je tato možnost nastavena na **Ne**. Dá se nastavit na **Ano** pouze v případě, že hodnota ve sloupci **Typ hlavního účtu** je **Rozvaha**, **Majetek** nebo **Závazek**. Když je možnost nastavena na **Ne**, počáteční zůstatky budou zaúčtovány souhrnně, jak je obvyklé při uzávěrce na konci roku. Pokud je nastaveno na **Ano**, budou podrobně vytvořeny počáteční zůstatky pro každou transakci hlavní knihy, která není zúčtována pro hlavní účet.

## <a name="year-end-close"></a>Roční uzávěrka

Když spustíte uzávěrku na konci roku tím, že půjdete do **Hlavní kniha** > **Uzavření období** > **Uzávěrka na konci roku**, proces vytvoří počáteční zůstatky pro hlavní účty, které jsou definovány pro vypořádání hlavní knihy. Počáteční zůstatky se vytvářejí buď souhrnně nebo podrobně, v závislosti na nastavení vypořádání hlavní knihy. Proces vylučuje transakce hlavní knihy, které jsou vypořádány, bez ohledu na to, zda účtujete počáteční zůstatek pro každý hlavní účet souhrnně nebo podrobně.

Například více transakcí je zaúčtováno na hlavní účet 130100 ve fiskálním roce 2021.

| Číslo deníku | Doklad  | Datum       | Typ      | Účet hlavní knihy | Název účtu        | Popis       | Měna | Částka v měně transakce | Částka  | Částka v měně vykazování |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 3. 12. 2021  | Aktivní | 130100-001-    | Pohledávky | Servisní poplatek       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 5. 12. 2021  | Aktivní | 130100-002-    | Pohledávky | Provozní náklady         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16. 12. 2021 | Aktivní | 130100-001-    | Pohledávky | Refundovat            | USD      | −100                           | −100    | −100                         |
| 20851          | ARP-8000 | 20. 12. 2021 | Aktivní | 130100-002-    | Pohledávky |                   | USD      | −0,88                          | −0,88   | −0,88                        |
| 20853          | ARPM0004 | 20. 12. 2021 | Aktivní | 130100-002-    | Pohledávky |                   | EUR      | −127,11                        | −174,12 | −174,12                      |
| 20856          | CMV-4010 | 21. 12. 2021 | Aktivní | 130100-002-    | Pohledávky | Kredit na účtu | USD      | −175                           | −175    | −175                         |
| 20857          | FTV-3011 | 28. 12. 2021 | Aktivní | 130100-001-    | Pohledávky | Provozní náklady         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29. 12. 2021 | Aktivní | 130100-002-    | Pohledávky | Služba           | USD      | 300                            | 300     | 300                          |

Z těchto transakcí jsou tři vypořádány během vypořádání hlavní knihy.

Existuje faktura na 175 USD. Tato faktura byla uhrazena platbou v eurech (EUR) a byla provedena platební sleva.

| Číslo deníku | Doklad  | Datum       | Typ      | Účet hlavní knihy | Název účtu        | Popis | Měna | Částka v měně transakce | Částka  | Částka v měně vykazování |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 5. 12. 2021  | Aktivní | 130100-002-    | Pohledávky | Provozní náklady   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 20. 12. 2021 | Aktivní | 130100-002-    | Pohledávky |             | USD      | −0,88                          | −0,88   | −0,88                        |
| 20853          | ARPM0004 | 20. 12. 2021 | Aktivní | 130100-002-    | Pohledávky |             | EUR      | −127,11                        | −174,12 | −174,12                      |

Výsledky pro hlavní účet 130100 závisí na tom, zda je funkce povolena před uzavřením na konci roku. Pokud je funkce povolena, závisí výsledek také na nastavení možnosti Zachovat detail během uzávěrky roku.

### <a name="the-feature-isnt-enabled"></a>Funkce není zapnutá
Uzavření na konci roku vytvoří tři transakce počátečního zůstatku pro hlavní účet 130100 v roce 2022. Součet transakcí v účetní měně je 525 USD.

| Číslo deníku | Doklad  | Datum     | Typ    | Účet hlavní knihy | Název účtu        | Popis | Měna | Částka v měně transakce | Částka  | Částka v měně vykazování |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-002-    | Pohledávky |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-001-    | Pohledávky |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-002-    | Pohledávky |             | EUR      | −127,11                        | −174,12 | −174,12                      |

I když byla transakce platby za −127,11 EUR vypořádána v hlavní knize, transakce stále projde jako počáteční zůstatek.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Funkce je povolena a Zachovat podrobnosti během uzávěrky na konci roku = Ne

Uzavření na konci roku vytvoří dvě transakce počátečního zůstatku pro hlavní účet 130100 v roce 2022. Součet transakcí v účetní měně je stále USD 525, ale transakce vypořádané v hlavní knize jsou vyloučeny z počátečního zůstatku. Celková částka pro účet 130100-002- je 125 USD místo 299,12 USD a transakce za 127,11 EUR / 174,12 USD je zcela vyloučena.

| Číslo deníku | Doklad  | Datum     | Typ    | Účet hlavní knihy | Název účtu        | Popis | Měna | Částka v měně transakce | Částka | Částka v měně vykazování |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-002-    | Pohledávky |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-001-    | Pohledávky |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Funkce je povolena a Zachovat podrobnosti během uzávěrky na konci roku = Ano

Uzavření na konci roku vytvoří pět transakcí počátečního zůstatku pro hlavní účet 130100 v roce 2022. Pro každou z pěti transakcí, které nebyly vypořádány, se vytvoří samostatná transakce počátečního zůstatku. Součet transakcí v účetní měně je stále 525 USD.

| Číslo deníku | Doklad  | Datum     | Typ    | Účet hlavní knihy | Název účtu        | Popis       | Měna | Částka v měně transakce | Částka | Částka v měně vykazování |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-001-    | Pohledávky | Servisní poplatek       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-001-    | Pohledávky | Refundovat            | USD      | −100                           | −100   | −100                         |
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-002-    | Pohledávky | Kredit na účtu | USD      | −175                           | −175   | −175                         |
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-001-    | Pohledávky | Provozní náklady         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Otevření | 130100-002-    | Pohledávky | Služba           | USD      | 300                            | 300    | 300                          |

Jsou-li uchovávány podrobnosti transakce, původní podrobné transakce nejsou ovlivněny. Zůstávají zaúčtovány a nevypořádány ve fiskálním roce, který se uzavírá. Kopie těchto transakcí se vytvoří pro počáteční zůstatek. Následující hodnoty z původních transakcí se zkopírují do transakcí počátečního zůstatku.

- Účet hlavní knihy (hlavní účet a všechny finanční dimenze)
- Částky v měně transakce, účtování a vykazování
- Popis
- Účtovací vrstva
- Typ zaúčtování

   > [!NOTE]
   > Žádné jiné transakce počátečního zůstatku nemají přiřazen typ účtování. Proto lze typ účtování použít k rozlišení počátečních transakcí, které byly podrobně předány.

Některá pole z původních transakcí se musí změnit v podrobných transakcích počátečního zůstatku. Datum transakcí počátečního zůstatku je vždy první den následujícího fiskálního roku. Číslo deníku se musí změnit a číslo dokladu se změní na hodnotu, která byla zadána v dialogovém okně uzavření konce roku.

Informace z původních transakcí naleznete na stránce **Vypořádání hlavní knihy**. Každá podrobná transakce počátečního zůstatku zobrazuje sloupec **Původní datum transakce** v mřížce. Tento sloupec vám může pomoci spárovat transakce v novém fiskálním roce. Můžete si vybrat **Zobrazit původní doklad** pro návrat k úplnému původnímu dokladu.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Vyrovnat transakce
Chcete-li vyrovnat transakce, postupujte takto.

1. Přejděte do nabídky **Hlavní kniha** > **Periodické úkoly** > **Vyrovnání hlavní knihy**.
2.  Nastavte filtry v horní části stránky.

    1. Vybrat rozsah dat Nebo můžete vybrat kód časového intervalu pro automatické vyplnění časového rozsahu.

       - Rozsah dat nemůže přesahovat fiskální roky. Pokud rozsah dat přesahuje fiskální roky, při výběru **Zobrazit transakce** se nezobrazí žádné transakce.
       - Pokud je rozsah dat v otevřeném fiskálním roce, transakce mohou být vypořádány a vypořádání může být zrušeno. Pokud je rozsah dat v uzavřeném fiskálním roce nebo pokud je uzávěrka na konci roku dokončena, transakce jsou zobrazeny, ale nelze je vypořádat ani zrušit. Zrušit označení transakcí můžete pouze v uzavřeném fiskálním roce. Pokud je rozsah dat v uzavřeném fiskálním roce, tlačítka **Označit vybrané**, **Vypořádat označené transakce** a **Vrátit označené transakce** nejsou k dispozici.

    2. Vyberte hlavní účet, jehož transakce chcete zobrazit. Toto pole je povinné. Vyhledávání zobrazí pouze hlavní účty, které jsou vybrány na stránce **Vypořádání účetní knihy** pro účtovou osnovu společnosti.
    3. Vyberte účtovací vrstvu. Nemůžete vypořádat transakce, které jsou v různých účtovacích vrstvách.
    4. Chcete-li zobrazit hlavní účet a dimenze v oddělených sloupcích, vyberte sadu finančních dimenzí.

3.  Vyberte **Zobrazit transakce** k zobrazení všech transakcí, které odpovídají vámi nastaveným filtrům. Pokud změníte jakýkoliv z filtrů nebo sad dimenzí, je nutné vybrat možnost **Zobrazit transakce** znovu.
4.  Vyberte řádky pro vyrovnání. Hodnota v poli **Vybraná částka** v horní části stránky se zvyšuje nebo snižuje o celkovou částku na vybraných řádcích.
5.  Po dokončení výběru transakcí vyberte **Označit vybrané**. Ve sloupci **Označené** se zobrazí zaškrtnutí pro každou vybranou transakci. Kromě toho se hodnota pole **Označená částka** nad mřížkou zvyšuje nebo snižuje o celkovou částku na označených řádcích.
6.  Když je hodnota v poli **Označená částka** rovna **0** (nule), vyberte **Vyrovnat označené transakce**.

    - Částečné vypořádání není povoleno. Nemůžete například vyrovnat 100 USD debetní transakci oproti 90 USD kreditní transakce. Zbývajících 10 USD kreditní transakce musí být také označeno pro zahrnutí do vypořádání.
    - Zadejte datum vypořádání. Datum musí být stejné nebo pozdější než poslední datum transakcí, které jsou označeny k vypořádání.

Stav označených transakcí je aktualizován na **Vyrovnáno**.

> [!IMPORTANT]
> Všechny transakce, které jste označili k vypořádání pro aktivní právnickou osobu a vybraný hlavní účet, budou vypořádány. Transakce se na stránce nemusí objevit. Budou vyrovnány, i když budou skryté kvůli filtru.

Některé procesy, jako je zrušení transakce, automaticky vypořádají transakce hlavní knihy. Například platba a faktura jsou vypořádány v pohledávkách a vypořádání generuje realizovaný zisk/ztrátu. Zúčtování platby a faktury nevypořádává žádné transakce hlavní knihy, jako jsou transakce pro účet hlavní knihy pohledávek. Pokud však platba a faktura nejsou zúčtované v Účtech, stornovací účetní zápis, který byl zaúčtován při stornování vypořádání pohledávek, způsobí, že původní a stornovací účetní zápisy budou vypořádány v hlavní knize. Když je zapnutá funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku**, nedojde k vypořádání storna automaticky, pokud je datum storna v jiném fiskálním roce.

## <a name="use-excel-for-ledger-settlement"></a>Pro vyúčtování účetní knihy použijte Excel

Transakce, které jsou zobrazeny na stránce **Vyúčtování účetní knihy** lze exportovat do Excelu. V Excelu můžete transakce dále filtrovat a určit, které transakce označit pro vypořádání.
Obě entity zúčtování hlavní knihy exportují transakce hlavní knihy pouze pro hlavní účet, který je vybrán na stránce **Vypořádání hlavní knihy**. Přestože transakce za uzavřené fiskální roky lze stále označit nebo odznačit pomocí Excelu, nelze je vypořádat. Navíc vypořádané transakce nelze pro daný fiskální rok stornovat.

## <a name="make-transactions-easier-to-find"></a>Snadnější vyhledání transakcí

Stránka **Vyrovnání hlavní knihy** obsahuje možnosti, které usnadňují zobrazení transakcí, které potřebujete pro vyrovnání.

•   Filtr **Označené** použijte k filtrování transakcí podle toho, zda je zaškrtávací políčko **Označené** pro danou položku zapnuto.
•   Filtr **Stav** použijte k filtrování transakcí na základě jejich stavu.
•   Vyberte možnost **Seřadit podle absolutní částky**, chcete-li seřadit částky podle absolutní hodnoty. Tímto způsobem můžete seskupit debety a kredity, které mají stejnou částku.

## <a name="reverse-a-settlement"></a>Stornování vyrovnání

Omylem provedené vyrovnání lze stornovat.

1.  Postupujte podle kroků 1 až 3 v části [Vypořádat transakce](#settle-transactions) pro zobrazení transakcí, které vás zajímají.
2.  Ve filtru **Stav** vyberte možnost **Vyrovnáno**.
3.  Vyberte řádky pro stornování.
4.  Vyberte **Stornovat označené transakce**. Stav všech transakcí, které mají stejné ID vypořádání, se aktualizuje na **Není vyřízeno**.

> [!IMPORTANT]
> Všechny transakce, které mají stejné ID vypořádání, budou stornovány, i když nejsou označeny. Například byly označeny a vypořádány čtyři řádky. Všechny čtyři řádky mají stejné ID vypořádání. Pokud označíte jeden z těchto čtyř řádků a poté vyberete **Stornovat označené transakce**, všechny čtyři řádky budou stornovány.






