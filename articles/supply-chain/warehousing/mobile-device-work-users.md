---
title: Uživatelské účty mobilního zařízení
description: Toto téma popisuje, jak nastavit a spravovat uživatelské účty, které umožňují pracovníkům přihlásit se a používat aplikaci skladu.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4cb36160e692cc12140b57037d2c9739f7b2ebd
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462663"
---
# <a name="mobile-device-user-accounts"></a>Uživatelské účty mobilního zařízení

[!include [banner](../includes/banner.md)]

Pokaždé, když pracovník začne používat aplikaci skladu, musí se přihlásit pomocí uživatelského jména a hesla. Ke každému pracovníkovi v systému lze přiřadit libovolný počet uživatelů skladové aplikace a sklady jsou obvykle přidruženy ke každému z těchto uživatelů skladové aplikace. Pro každého pracovníka jsou také nakonfigurovány různé možnosti pro vytvoření výchozích nastavení a dalších nastavení, která jsou relevantní pro používání aplikace skladu.

## <a name="set-up-the-required-worker-and-employee-records"></a>Nastavte požadovanou evidenci pracovníků a zaměstnanců

Než budete moci nastavit uživatele skladové aplikace, každý pracovník již musí existovat jako zaměstnanec Supply Chain Management nebo pracovník v modulu **Human Resources**.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Nastavení uživatelských účtů mobilního zařízení

Po nastavení požadovaných pracovníků a zaměstnanců v Human Resourcces můžete ke každému z nich přiřadit uživatele aplikace skladu a nastavit další možnosti, které ovlivní, jak mohou aplikaci používat.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Pracovník**.
1. Chcete-li upravit existujícího pracovníka, vyberte ho v podokně seznamu. V podokně Akce volbou **Nový** přidáte nový záznam.
1. Pokud nastavujete nového pracovníka, postupujte takto:

    1. V poli **Pracovník** vyberte cílového uživatele v seznamu zaměstnanců.
    1. Zvolte **Zvolit**.
    1. V podokně akcí vyberte **Uložit**.

1. Výchozí profil lze použít k vedení skladníka na balicí stanici procesem, který je tam vyžadován. Alternativně lze výchozí profil použít k uložení preferovaného nastavení profilu pro pracovníka. Na záložce **Profil** zadejte následující pole:

    - **Zásady balení kontejnerů** – Vyberte zásady balení kontejnerů, které definují, jak mají být kontejnery na balicí stanici zpracovávány. Zásady balení kontejnerů, které jsou zde vybrány, budou pro pracovníka předem vybrány, když otevře balicí stanici. Další informace naleznete v následujícím příspěvku na blogu: [Vylepšená funkce balení](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611),
    - **ID profilu balení** – Vyberte ID profilu balení, které definuje použité zásady balení a nastavení kontejneru. Pokud je vybrané ID profilu balení přidruženo k zásadám balení kontejneru, nebudete moci změnit nastavení **Zásady balení kontejnerů** na této stránce.

1. Na pevné záložce **Výchozí balicí stanice** nastavte následující pole, abyste definovali výchozí balicí stanici, která se použije, když se pracovník přihlásí. V případě potřeby může pracovník stále vybrat jinou balicí stanici.

    - **Pracoviště** – Vyberte místo, kde se nachází výchozí balicí stanice.
    - **Sklad** – Vyberte sklad, kde se nachází výchozí balicí stanice.
    - **Umístění** – Vyberte umístění výchozí balicí stanice.

1. Pevná záložka **Uživatelé** umožňuje vytvořit libovolný počet uživatelských účtů aplikace skladu pro vybraného pracovníka. Každý účet je spojen s konkrétním skladem nebo sklady. Pomocí panelu nástrojů můžete přidat nebo odebrat uživatelské účty, resetovat heslo pro vybraný účet nebo přiřadit sklady k vybranému účtu. Pro každý uživatelský účet nastavte následující pole:

    - **ID uživatele** – Zadejte jedinečný identifikátor.
    - **Uživatelské jméno** – Zadejte název pro ID.
    - **Výchozí sklad** – Nastavte výchozí sklad, kde pracovník obvykle pracuje. Pomocí panelu nástrojů můžete přiřadit další sklady a pracovník může mezi sklady přepínat pomocí nepřímé aktivity **Změna skladu** položky nabídky mobilního zařízení.
    - **Název nabídky** – Vyberte kořenovou nabídku, která bude výchozí stránkou pro pracovníka. Možnost nastavit kořenovou nabídku pro každého pracovníka je užitečná, protože vám umožňuje ovládat strukturu nabídky, kterou může každý pracovník používat. Například nabídku pro pracovníky, kteří jsou aktivní pouze v odchozí oblasti, lze přizpůsobit pro úkoly související s odchozími operacemi pro danou oblast.
    - **Neaktivní** – Zaškrtnuté políčko označuje, že uživatelský účet je neaktivní. Uživatelský účet se automaticky deaktivuje, pokud pracovník zadá v aplikaci sklad pětkrát za sebou špatné heslo. Toto zaškrtávací políčko je také možné vybrat ručně. Zrušte zaškrtnutí, aby byl uživatel znovu aktivní.

1. Na pevné záložce **Práce** nastavte následující pole:

    - **Povolit přepsání místa výběru** – Nastavte tuto možnost na *Ano*, aby pracovník mohl přepsat místo pro vychystávání. Tato funkce může být užitečná, pokud fyzické zásoby neodpovídají umístění navrženému systémem.
    - **Povolit přepsání místa uložení** – Nastavte tuto možnost na *Ano*, aby pracovník mohl přepsat místo pro uložení. Tato funkce může být užitečná, pokud je navrhované umístění uložení aktuálně plné nebo není k dispozici, nebo pokud se umístění uložení změnilo.
    - **Povolit prodej před vychystáváním** – Nastavte tuto možnost na *Ano*, aby pracovník mohl při vychystávání prodejních objednávek nadměrně vychystávat. Další informace viz [Nadměrné vychystávání prodejních objednávek a převodních příkazů](over-picking-for-sales-and-transfer-orders.md)
    - **Povolit nadměrné vychystávání převodních příkazů** – Nastavte tuto možnost na *Ano*, aby pracovník mohl při vychystávání převodních příkazů nadměrně vychystávat. Další informace viz [Nadměrné vychystávání prodejních objednávek a převodních příkazů](over-picking-for-sales-and-transfer-orders.md)
    - **Povolit pohyb zásob s přidruženou prací** – Nastavte tuto možnost na *Ano*, abyste umožnili pracovníkovi přesunout zásoby, které jsou již rezervované nebo již spojené s jinou prací. Další informace viz [Pohyb zásob s přidruženou prací ve Warehouse Management](move-inventory-associated-work.md).
    - **Povolit ruční přerozdělení položek** – Nastavte tuto možnost na, *Ano*, abyste umožnili ruční přerozdělení pro pracovníka během krátkého vychystávání. Přerozdělení položek vede pracovníky k výběru inventáře z jiného místa. Přestože automatické přerozdělení je dostupné pro všechny pracovníky, ruční přerozdělení vyžaduje explicitní nastavení pro pracovníka. Schopnost řídit ruční přerozdělení pro každého pracovníka může být užitečná, protože vám umožňuje ovládat viditelnost, kterou má každý pracovník, když je například vybírání položek z karantény nebo hromadné oblasti omezeno na důvěryhodné pracovníky. Další informace naleznete v následujícím příspěvku na blogu: [Automatické a manuální přerozdělení položek během krátkého vychystávání](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Je nadřízeným počtu cyklů** – Nastavte tuto možnost na *Ano*, aby se z pracovníka stal nadřízený počtu cyklů. V tomto případě budou všechny počty cyklů, které pracovník provede ve skladové aplikaci, okamžitě schváleny. Pole **Maximální procentuální limit**, **Limit maximálního množství** a **Limit maximální hodnoty** se neberou v úvahu pro pracovníky, pro které je tato možnost nastavena na *Ano*.
    - **Maximální procentuální limit** – Zadejte nejvyšší limit procent, o který se počet cyklů může lišit od očekávaného počtu bez schválení nadřízeným cyklické inventury.
    - **Limit maximálního množství** – Zadejte celkové množství, o které se zadané množství může lišit od očekávaného množství (v jednotkách), aniž by bylo vyžadováno schválení nadřízeným počítání cyklů.
    - **Limit maximální hodnoty** – Zadejte maximální částku, o kterou se náklady zásob mohou lišit od očekávaných nákladů bez schválení nadřízeným cyklické inventury.

1. V podokně akcí vyberte **Uložit**.
1. Pokud jste přidali nový uživatelský účet, zobrazí se dialogové okno **Nastavit heslo**, ve kterém můžete vytvořit jednoduché heslo, pomocí něhož se uživatel může přihlásit k mobilní aplikaci. Dvakrát zadejte jednoduché heslo a poté vyberte **Uložit heslo** pro pokračování.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Nastavte jazyk, formáty čísel a časové pásmo pro každého uživatele aplikace skladu

Když se pracovník přihlásí do mobilní aplikace Warehouse Management, změní se jazyk, formáty čísel a časové pásmo tak, aby odpovídaly preferencím daného pracovníka. Nastavení účtu pro pracovníka, který je vybrán v kroku 3 v části [Nastavení uživatelských účtů mobilního zařízení](#set-wma-users) určuje použitá nastavení. Pokud požadujete samostatné nastavení pro každého uživatele, použijte různé pracovní účty. Následující postup ukazuje, jak změnit jazyk, formáty čísel a časové pásmo pro každého uživatele aplikace skladu.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Pracovník**.
1. Najděte jméno pracovníka, kterého chcete nastavit. Ujistěte se, že pracovník má všechny požadované uživatelské účty aplikace skladu, které jsou uvedeny na pevné záložce **Uživatelé**. Podle potřeby vytvořte nového pracovníka nebo přidejte uživatelské účty aplikace skladu podle kroků v části [Nastavení uživatelských účtů mobilního zařízení](#set-wma-users).
1. Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé**.
1. Vyberte uživatelský účet, kde sloupec **Osoba** zobrazuje jméno pracovníka, kterého jste našli v kroku 2.

    > [!IMPORTANT]
    > Hodnoty **ID uživatele**, které jsou uvedeny na stránce **Uživatelé**, *nesouvisejí* s hodnotou, která je zobrazena na pevné záložce **Uživatelé** stránky **Pracovník**, kterou jste otevřeli v kroku 1.

1. V podokně akcí vyberte volbu **Možnosti uživatele**.
1. Na kartě **Předvolby** natavte následující pole:

    - **Jazyk** – Vyberte jazyk, který pracovník preferuje. Toto pole také řídí formát čísla, které se zobrazuje v aplikaci skladu.
    - **Formát data, času a čísla** – Vyberte formát data a času, kterému pracovník dává přednost. Skladová aplikace používá číselný formát spojený s jazykem vybraným v poli **Jazyk** místo tohoto nastavení.
    - **Časové pásmo** – Vyberte časové pásmo, ve kterém pracovník pracuje. Toto pole ovlivňuje časové razítko pro všechny registrace, které pracovník pomocí aplikace provede.

> [!NOTE]
> V některých případech aplikace skladu nebude schopna najít konkrétní nastavení pracovníka, která určují jazyk, formáty čísel a časové pásmo. Platí následující pravidla:
>
> - Pokud aplikace není připojena k prostředí Supply Chain Management (například při prvním spuštění aplikace po její instalaci), použije se jazyk místního zařízení. Když se změní jazyk zařízení, změní se také jazyk aplikace. Další informace o konfiguraci jazyka pro místní zařízení naleznete v dokumentaci k vašemu zařízení nebo operačnímu systému.
> - Pokud je aplikace připojena k prostředí Supply Chain Management, ale pro přihlášeného pracovníka nejsou nastaveny žádné předvolby, jazyk, formáty čísel a časové pásmo se vyberou na základě účtu přidruženého k ID klienta, které zařízení používá pro připojení k Supply Chain Management. Další informace viz [Vytvoření a konfigurace uživatelských účtů v aplikaci Supply Chain Management](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Pokud si všimnete, že se u registrací provedených pomocí aplikace skladu zobrazují nesprávná časová razítka, možná budete muset upravit časové pásmo nastavené pro uživatelský účet, který pracovníci používají k přihlášení nebo ověření pomocí Supply Chain Management. Jak již bylo zmíněno, nastavení časového pásma může pocházet z uživatelského účtu, který se používá k přihlášení do aplikace skladu, jak je nastaveno na stránce **Pracovník**. Případně, pokud uživatelský účet není nastaven na stránce **Pracovník**, časové pásmo pochází z uživatelského účtu, který je přidružen k ID klienta, které se používá pro ověřování, jak je nastaveno na stránce **[Aplikce Azure Active Directory](install-configure-warehouse-management-app.md)**.
