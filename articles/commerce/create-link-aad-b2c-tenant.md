---
title: Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure
description: Tento článek popisuje, jak vytvořit nebo propojit existujícího tenanta Azure Active Directory (Azure AD) typu business-to-consumer (B2C) v portálu Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785227"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit nebo propojit tenanta Azure Active Directory (Azure AD) typu business-to-consumer (B2C) v portálu Microsoft Azure. Další informace naleznete v tématu [Kurz: Vytvoření tenanta Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-create-tenant).

Pro vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure postupujte následovně.

1. Přihlaste se do [portálu Azure](https://portal.azure.com/).
1. Z nabídky portálu Azure vyberte možnost **Vytvořit prostředek**. Ujistěte se, že používáte předplatné a adresář, který bude připojen k vašemu prostředí Commerce.

    ![Vytvoření prostředku na portálu Azure.](./media/B2CImage_1.png)

1. Přejděte na **Identita \> Azure Active Directory B2C**.
1. Na stránce **Vytvoření nového klienta B2C nebo připojení k existujícímu klientovi** použijte jednu z následujících možností, které nejlépe vyhovují potřebám vaší společnosti:

    - **Vytvořit nového tenanta Azure AD B2C**: Touto možností vytvoříte nového tenanta Azure AD B2C.
        1. Vyberte **Vytvořit nového klienta Azure AD B2C**.
        1. Pro **Název organizace** zadejte název organizace.
        1. Pro **Počáteční název domény** zadejte počáteční název domény.
        1. Pro **Země nebo oblast** vyberte zemi nebo oblast.
        1. Volbou **Vytvořit** vytvoříte klienta.

     ![Vytvoření nového klienta Azure AD.](./media/B2CImage_2.png)

     - **Propojit existujícího klienta Azure AD B2C s mým předplatným Azure**: Tuto možnost použijte, pokud již existuje klient Azure AD B2C, který chcete propojit.
        1. Vyberte **Propojit existujícího klienta Azure AD B2C s mým předplatným Azure**.
        1. Pro **Klient Azure AD B2C** vyberte příslušného klienta B2C. Pokud se v oblasti výběru zobrazí zpráva „Nebyly nalezeni žádní oprávnění klienti B2C“, nemáte žádného existující oprávněného klienta B2C a budete muset vytvořit nového.
        1. Pro **Skupina prostředků** vyberte možnost **Vytvořit novou**. Zadejte **Název** pro skupinu prostředků, která bude obsahovat klienta, vyberte **Umístění skupiny prostředků** a pak vyberte možnost **Vytvořit**.

    ![Propojení existujícího klienta Azure AD B2C s předplatným Azure.](./media/B2CImage_3.png)

1. Po vytvoření nového adresáře Azure AD B2C (což může chvíli trvat) se na řídicím panelu zobrazí odkaz na nový adresář. Tento odkaz vás přesměruje na stránku „Vítá vás Azure Active Directory B2C“.

    ![Odkaz na nový adresář Azure AD](./media/B2CImage_4.png)

> [!NOTE]
> Pokud máte více předplatných v rámci účtu Azure nebo jste zřídili klienta B2C bez propojení s aktivním předplatným, banner **Řešení potíží** vás nasměruje k propojení klienta a předplatného. Vyberte zprávu řešení potíží a podle pokynů vyřešte problém s předplatným.

Na následujícím obrázku je znázorněn příklad banneru **Řešení potíží** v Azure AD B2C.

![Upozornění, že adresář nemá žádné aktivní předplatné.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu nastavení B2C tenanta v Commerce, pokračujte na [Vytvoření aplikace B2C](create-b2c-app.md).

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md)

[Vytvoření aplikace B2C](create-b2c-app.md)

[Vytvoření zásad toku uživatele](create-user-flow-policies.md)

[Přidání zprostředkovatelů sociální identity (volitelné)](add-social-identity-providers.md)

[Aktualizace Commerce Headquarters o nové informace Azure AD B2C](update-hq-aad-b2c-info.md)

[Konfigurace klienta B2C v konfigurátoru webů Commerce](config-b2c-tenant-site-builder.md)

[Doplňkové informace o B2C](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
