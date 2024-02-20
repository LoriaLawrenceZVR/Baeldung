<h1><strong>1. Overview</strong></h1>
<p>This document will cover the following <strong>annotations of the Mockito library:</strong> @Mock, @Spy, @Captor and @InectMocks</p>


<hr>


<h1><strong>2. Enable Mockito Annotations</strong></h1>
<p>There are different ways to enable the use of annotations with Mockito tests.</p>

<h2><strong>2.1. MockitoJUnitRunner</strong></h2>
<p>The first option we have is to <strong>annotate the JUnit test with a MockitoJUnitRunner</strong></p>

~~~
@ExtendWith(MockitoExtension.class)
public class MockitoAnnotationUnitTest {
    ...
}
~~~

<h2><strong>2.2. MockitoAnnotations.openMocks()</strong></h2>
<p>Alternatively, we can <strong>enable Mockito annotations programmatically</strong> by invoking MockitoAnnotations.openMocks():</p>

~~~
@BeforeEach
public void init() {
    MockitoAnnotations.openMocks(this);
}
~~~

<h2><strong>2.3. MockitoJUnit.rule()</strong></h2>
<p>Lastly, we can use a <strong>MockitoJUnit.rule():</strong></p>

~~~
public class MockitoAnnotationsInitWithMockitoJUnitRuleUnitTest {

    @Rule
    public MockitoRule initRule = MockitoJUnit.rule();

    ...
}
~~~

<p>In this case, we must remember to make our rule public.</p>


<hr>


<h1><strong>3. @Mock Annotation</strong></h1>
<p>The most widely used annotation in Mockito is @Mock. We can use @Mock to create and inject mocked instances without having to call Mockito.mock manually.</p>
<p>In the following example, we’ll create a mocked ArrayList manually without using the @Mock annotation:</p>

~~~
@Test
public void whenNotUseMockAnnotation_thenCorrect() {
    List mockList = Mockito.mock(ArrayList.class);
    
    mockList.add("one");
    Mockito.verify(mockList).add("one");
    assertEquals(0, mockList.size());

    Mockito.when(mockList.size()).thenReturn(100);
    assertEquals(100, mockList.size());
}
~~~
