# testdata
@Test
	public void ChatPage() throws InterruptedException {
		
		Log.info("Driver Start And Login");
		Home hp = PageFactory.initElements(driver, Home.class);
		hp.chat();
		
		Log.info("Chat Page");
		ChatPage cp = PageFactory.initElements(driver, ChatPage.class);

		WebDriverCommonLib wb = PageFactory.initElements(driver, WebDriverCommonLib.class);
		wb.select(cp.navigatetochat(), "Petco");
		cp.startchat();

	}
}
