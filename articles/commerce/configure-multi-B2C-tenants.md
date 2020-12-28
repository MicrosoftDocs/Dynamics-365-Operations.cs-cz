---
title: Konfigurace několika klientů typu B2C v prostředí obchodu
description: Toto téma popisuje, kdy a jak nastavit vícen klientů typu business-to-consumer (B2C) Microsoft Azure Active Directory (Azure AD) na kanál pro ověření uživatele ve vyhrazeném prostředí Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: da27e3ed0a0e50126590609d09575befe17a7aa2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517109"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Konfigurace několika klientů typu B2C v prostředí obchodu

[!include [banner](includes/banner.md)]

Toto téma popisuje, kdy a jak nastavit vícen klientů typu business-to-consumer (B2C) Microsoft Azure Active Directory (Azure AD) na kanál pro ověření uživatele ve vyhrazeném prostředí Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Dynamics 365 Commerce používá službu cloudové identity typu B2C Azure AD k podpoře uživatelských pověření a toků ověřování. Uživatelé mohou použít ověřovací toky k přihlášení, přihlášení a resetování hesla. B2C Azure AD ukládá citlivé informace o ověřování uživatele (například jeho uživatelské jméno a heslo). Uživatelský záznam je jedinečný pro každého klienta B2C a používá buď pověření uživatelského jména (e-mailová adresa) nebo pověření poskytovatele sociálních identit.

Ve většině případů se v prostředí Commerce používá jediný klient B2C Azure AD. Zákazníci v Commerce mohou poté vytvářet a publikovat více pracovišť ve stejném prostředí Commerce a na těchto webech budou používat stejná pověření zákazníka. Pokud je však pracoviště v prostředí považováno za různé značky a zobrazují se uživatelům jako samostatné podniky, může být pro kanál, který se používá pro oddělení pracoviště/značky, nakonfigurován klient B2C.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Důležité informace o nastavení více B2C klientů na kanál

Pokud je každý kanál nebo pracoviště považováno za samostatnou firmu, nejlepším způsobem, s ohledem na ověřovací toky uživatelů v obchodu, je použití oddělených právnických osob. Chcete-li však ponechat každý kanál nebo web ve stejném prostředí a právnické osobě, ale chcete mít pro každé pracoviště samostatné ověřování uživatelů, je důležité zvážit následující body, než budete pokračovat:

- Uživatelé budou mít pro každý kanál nebo pracoviště vlastní odlišná pověření.

    Stejná osoba může mít dva oddělené účty na kanál nebo web, protože každý účet bude jedinečným vstupem do samostatného klienta B2C.

- V prostředí Microsoft Dynamics budou pro hledání v globálních záznamech vráceny samostatné záznamy odběratelů.

    Pokud uživatel používá stejnou e-mailovou adresu v rámci kanálů nebo pracovišť, vrátí globální vyhledávání zákazníků výsledky pro každý kanál nebo Web. (Zobrazí se indikátor kanálu.)

- Adresář lze použít k usnadnění seskupení uživatelů, aby bylo možné je sledovat podle jednotlivých kanálů.
- Počet záznamů odběratelů na kanál se může zvýšit a tento nárůst může ovlivnit výkon globálních hledání zákazníků.
- Klienti B2C musí být pečlivě mapováni na kanál, aby se předešlo situacím, kdy se odběratelé zaregistrují pro nesprávného klienta. V opačném případě může dojít k nejasnostem nebo sledování problémů.

Následující ilustrace znázorňuje několik B2C klientů v prostředí obchodu.

![Několik klientů typu B2C v prostředí Commerce](media/MultiB2C_In_Environment.png)

Pokud se rozhodnete, že váš podnik vyžaduje jedinečné B2C klienty na kanál ve stejném Commerce prostředí, požádejte o tuto funkci postupy uvedené v následujících oddílech.

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a>Požadavek, aby byl ve vašem prostředí povolen B2C pro kanál

V případě, že chcete, aby byl k dispozici samostatný B2C klient na kanál ve stejném Commerce Environment, musíte odeslat žádost Dynamics 365 Commerce. Další informace naleznete v tématech [Získání podpory pro Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) nebo diskutujte o vašem problému s kontaktem pro Commerce.

## <a name="configure-b2c-tenants-in-your-environment"></a>Konfigurovat klienty B2C ve vašem prostředí

Chcete-li konfigurovat klienta typu B2C ve vašem prostředí, proveďte příslušné postupy v této části.

### <a name="add-an-azure-ad-b2c-tenant"></a>Přidejte klienta B2C Azure AD

Chcete-li do prostředí přidat klienta B2C Azure AD, postupujte podle následujících kroků.

1. Přihlaste se ke konfigurátoru webů Commerce pro vaše prostředí jako správce systému. Chcete-li konfigurovat klienta B2C Azure AD, musíte být správcem systému pro prostředí Commerce.
1. V levém navigačním podokně vyberte **Nastavení klienta** a rozbalte je.
1. Vyberte **Nastavení B2C** a poté vyberte **Spravovat**.
1. Vyberte **Přidat aplikaci B2C** a poté zadejte následující informace:

    - **Název aplikace**: zadejte název, který má být použit pro aplikaci v kontextu jeho správy ve službě Commerce. Doporučujeme, abyste používali název aplikace, který jste zvolili při nastavení aplikace Azure AD B2C na portálu Azure. Tímto způsobem lze omezit záměnu při správě B2C klientů ve službě Commerce.
    - **Název klienta**: zadejte název klienta B2C, jak se objevuje na portálu Azure.
    - **Zapomenout ID zásad hesla**: Zadejte ID zásad (název zásady na portálu Azure).
    - **ID zásady registrace a přihlášení**: Zadejte ID zásad (název zásady na portálu Azure).
    - **GUID klienta**: zadejte ID klienta B2C Azure AD tak, jak se objevuje na portálu Azure (ne v ID aplikace pro klienta B2C).
    - **ID zásad úprav profilu**: Zadejte ID zásad (název zásady na portálu Azure).

1. Až tyto informace dokončíte, výběrem **OK** uložte provedené změny.

> [!NOTE]
> Pole **Rozsah**, **ID neinteraktivních zásad**, **ID neinteraktivních klientů**, **Vlastní doména přihlašování** a **ID zásad registrace** ponechte prázdná, pokud vám tým Dynamics 365 Commerce neřekne, abyste je nastavili.
Váš nový klient B2C Azure AD by se nyní měl objevit v seznamu v části **Spravovat aplikace B2C**.

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Správa nebo odstranění klienta B2C Azure AD

1. Přihlaste se ke konfigurátoru webů Commerce pro vaše prostředí jako správce systému. Chcete-li konfigurovat klienta B2C Azure AD, musíte být správcem systému pro prostředí Commerce.
1. V levém navigačním podokně vyberte **Nastavení klienta** a rozbalte je.
1. Vyberte **Nastavení B2C** a poté vyberte **Spravovat**.
1. Chcete-li upravit B2C klienta, vyberte symbol tužky vedle něj. Chcete-li odstranit klienta B2C, vyberte symbol odpadkového koše.
1. Vyberte **Uložit** a potom **Publikovat** pro aktivaci svých změn.

> [!WARNING]
> Pokud je klient B2C nakonfigurován pro aktivní nebo publikovaný web, mohou se uživatelé přihlásili pomocí účtů, které jsou k dispozici v klientovi. Odstraníte-li nakonfigurovaného klienta v nabídce **Nastavení klienta \> Klient B2C**, odeberte přidružení tohoto klienta B2C z webů, které jsou přidruženy ke všem kanálům klienta. V takovém případě se může stát, že uživatelé již nebudou schopni přihlásit se ke svým účtům. Proto při odstraňování nakonfigurovaného klienta buďte velmi opatrní.
>
> Po odstranění nakonfigurovaného klienta budou i nadále udržovat klienta B2C a záznamy, ale konfigurace systému Commerce pro daného klienta bude změněna nebo odebrána. Uživatelé, kteří se pokusí zaregistrovat nebo se přihlásit k webu, vytvoří nový záznam účtu ve výchozím nebo nově přidruženém klientovi B2C, který je nakonfigurován pro kanál webu.
## <a name="configure-your-channel-with-a-b2c-tenant"></a>Nakonfigurujte kanál pomocí klienta B2C

1. Přihlaste se ke konfigurátoru webů Commerce pro vaše prostředí jako správce systému. Chcete-li konfigurovat klienta B2C Azure AD, musíte být správcem systému pro prostředí Commerce.
1. V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.
1. Vyberte **Kanály** a poté vyberte kanál, který chcete konfigurovat.
1. V podokně vlastnosti vpravo v poli **Vybrat aplikaci B2C** vyberte pro tento kanál konfigurovaného klienta B2C Azure AD pro použití v tomto kanálu.
1. V řádku příkazů výběrem možnosti **Uložit a publikovat** potvrďte novou nebo aktualizovanou konfiguraci.

> [!WARNING]
> Pokud změníte aplikaci B2C, která je přiřazena kanálu, odstraníte aktuální odkazy, které byly vytvořeny pro všechny uživatele, kteří se již v prostředí registrovali. V tomto případě nebudou mít uživatelé k dispozici žádná pověření přidružená k aktuálně přiřazené B2C aplikaci. Konfiguraci B2C kanálů Azure AD proto měňte pouze v případě, že jste kanál poprvé nastavili a žádní uživatelé se nemohou registrovat. V opačném případě se může stát, že se uživatelé budou muset znovu přihlásit, aby vytvořili záznam v novém klientovi B2C Azure AD.
## <a name="additional-resources"></a>Další prostředky

[Konfigurace názvu domény](configure-your-domain-name.md)

[Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md)

[Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)
