# RestTemplate


- **Requisição GET**
    
    String	endpoint	=	"http://localhost:8080/api/livros";
		  
    RestTemplate	restTemplate	=	new	RestTemplate();
    MultiValueMap<String,	String>	headers	=	new	LinkedMultiValueMap<>();
    headers.add("Authorization",	"Basic	"	+	credenciais.getCredenciaisBase64());
    
    RequestEntity<Object>	request	=	new	RequestEntity<Object>(headers, HttpMethod.GET,	URI.create(endpoint));
    ResponseEntity<Livro[]>	resposta	=	restTemplate.exchange(request,	Livro[].class);
    System.out.println(resposta.getBody());
    
 
